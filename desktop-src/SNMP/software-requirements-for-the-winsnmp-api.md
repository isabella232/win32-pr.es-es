---
title: Requisitos de software para la API de WinSNMP
description: Una aplicación WinSNMP debe tener acceso a la API de WinSNMP a través de la biblioteca de vínculos dinámicos WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cf78c4937996a44b2a82ebeb0b2963f9a4ffaada0288068b07cd3b60432c70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886075"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Requisitos de software para la API de WinSNMP

Una aplicación WinSNMP debe tener acceso a la API de WinSNMP a través de la biblioteca de vínculos dinámicos WSNMP32.DLL.

Los siguientes archivos son necesarios para admitir la funcionalidad de la API de WinSNMP.



| Nombre de archivo     | Descripción                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. Lib  | Biblioteca WinSNMP                                                                              |
| WSNMP32.DLL  | Proporciona la interfaz WinSNMP                                                                   |
| WINSNMP. H    | Archivo de encabezado WinSNMP                                                                          |
| SNMPTRAP.EXE | Recibe capturas de SNMP y las reenvía a MGMTAPI.DLL, la biblioteca de API de Microsoft SNMP Manager |
| SNMPAPI.DLL  | Proporciona utilidades SNMP                                                                      |



 

 

 




