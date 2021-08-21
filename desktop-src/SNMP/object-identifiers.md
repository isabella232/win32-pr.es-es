---
title: Identificadores de objeto (SNMP)
description: Un identificador de objeto SNMP nombra de forma única un objeto e identifica su ubicación dentro de una estructura de árbol de Base de información de administración (MIB).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b81d52e43cb3be89551dd597bc5084d533f3913264f8bcf5c0a2ef7dbb375bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009263"
---
# <a name="object-identifiers-snmp"></a>Identificadores de objeto (SNMP)

Un identificador de objeto SNMP nombra de forma única un objeto e identifica su ubicación dentro de una estructura de árbol de Base de información de administración (MIB). Los identificadores de objeto son tipos de datos de notación de sintaxis abstracta one (ASN.1) independientes de la aplicación que constan de una secuencia de enteros no negativos o subidentificadores. Los identificadores de objeto deben tener un mínimo de dos subidentificadores y no deben superar los 128 subidentificadores.

El entorno de programación WinSNMP usa la [**estructura smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) para administrar los identificadores de objeto. El formato de la matriz de identificadores de objeto en una **estructura smiOID** es un subidentificador por elemento de matriz.

La representación de cadena numérica de puntos de un identificador de objeto separa sus subidentificadores con puntos; por ejemplo, "1.2.3.4.5.6".

Para obtener más información, vea La base de información de administración [de SNMP (MIB)](the-snmp-management-information-base-mib-.md) y las RFC pertinentes.

 

 




