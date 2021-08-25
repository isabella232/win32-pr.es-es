---
title: Marcas de enumeración
description: Marcas de enumeración
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeración
- Marcas de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa99352db877cdaef3d5297d754d1e66bb246240074cfc741ba3baff94a5d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910275"
---
# <a name="enumeration-flags"></a>Marcas de enumeración



| Constante               | Value      | Descripción                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| RTM \_ ENUM \_ START       | 0x00000000 | Enumerar rutas o destinos a partir de 0/0.                                                                                                         |
| RTM \_ ENUM \_ NEXT        | 0x00000001 | Enumerar rutas o destinos a partir de la longitud de la dirección o máscara especificada (por ejemplo, 10/8). La enumeración continúa hasta el final de la tabla de enrutamiento. |
| INTERVALO \_ DE ENUMERACIÓN \_ RTM       | 0x00000002 | Enumerar rutas o destinos en el subárbol especificado especificado por la longitud de la dirección o máscara (por ejemplo, 10/8).                                            |
| RTM \_ ENUM \_ ALL \_ DESTS  | 0x00000000 | Devuelve todos los destinos.                                                                                                                                  |
| RTM \_ ENUM \_ OWN \_ DESTS  | 0x01000000 | Devuelve solo los destinos que posee el cliente.                                                                                                      |
| ENUMERACIÓN RTM \_ \_ TODAS LAS \_ RUTAS | 0x00000000 | Devuelve todas las rutas.                                                                                                                                        |
| RUTAS \_ PROPIAS DE \_ \_ ENUMERACIÓN RTM | 0x00010000 | Devuelve solo las rutas que posee el cliente.                                                                                                            |



 

 

 




