---
title: Identificadores de objeto (SNMP)
description: Un identificador de objeto SNMP asigna un nombre único a un objeto e identifica su ubicación dentro de una estructura de árbol de la base de datos de información de administración (MIB).
ms.assetid: b4552185-ef37-4e04-9b19-a226165e0b32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed1f54f67b85000e508dddb42b9c784628a53ab
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103800649"
---
# <a name="object-identifiers-snmp"></a>Identificadores de objeto (SNMP)

Un identificador de objeto SNMP asigna un nombre único a un objeto e identifica su ubicación dentro de una estructura de árbol de la base de datos de información de administración (MIB). Los identificadores de objeto son tipos de datos de notación de sintaxis abstracta (ASN. 1) independientes de la aplicación que se componen de una secuencia de enteros no negativos o de subidentificadors. Los identificadores de objeto deben tener un mínimo de dos subidentificadors y no deben superar los 128 subidentificadors.

El entorno de programación WinSNMP utiliza la estructura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) para administrar los identificadores de objeto. El formato de la matriz de identificadores de objeto en una estructura **smiOID** es un subidentificador por elemento de matriz.

La representación de cadena numérica con puntos de un identificador de objeto separa sus subidentificadors con puntos; por ejemplo, "1.2.3.4.5.6".

Para obtener más información, consulte [la base de datos de información de administración (MIB) de SNMP](the-snmp-management-information-base-mib-.md) y las RFC pertinentes.

 

 




