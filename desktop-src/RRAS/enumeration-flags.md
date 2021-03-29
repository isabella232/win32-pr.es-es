---
title: Marcas de enumeración
description: Marcas de enumeración
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeración
- Marcas de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994237"
---
# <a name="enumeration-flags"></a>Marcas de enumeración



| Constante               | Value      | Descripción                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inicio de la \_ enumeración RTM \_       | 0x00000000 | Enumerar rutas o destinos a partir de 0/0.                                                                                                         |
| \_siguiente enumeración RTM \_        | 0x00000001 | Enumerar rutas o destinos a partir de la longitud especificada de máscara/dirección (por ejemplo, 10/8). La enumeración continúa hasta el final de la tabla de enrutamiento. |
| \_intervalo enum de RTM \_       | 0x00000002 | Enumerar rutas o destinos en el subárbol especificado especificados por la longitud de dirección/máscara (por ejemplo, 10/8).                                            |
| \_enumeración de \_ todos los \_ DESTs de RTM  | 0x00000000 | Devuelve todos los destinos.                                                                                                                                  |
| \_destino enum \_ de la versión RTM \_  | 0x01000000 | Devuelve solo los destinos que posee el cliente.                                                                                                      |
| versión RTM \_ enumerar \_ todas las \_ rutas | 0x00000000 | Devuelve todas las rutas.                                                                                                                                        |
| las \_ rutas de enumeración de RTM son \_ propias \_ | 0x00010000 | Devuelve solo las rutas que posee el cliente.                                                                                                            |



 

 

 




