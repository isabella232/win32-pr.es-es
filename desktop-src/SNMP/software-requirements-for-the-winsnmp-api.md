---
title: Requisitos de software para la API WinSNMP
description: Una aplicación WinSNMP debe tener acceso a la API WinSNMP a través de la biblioteca de vínculos dinámicos WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268248"
---
# <a name="software-requirements-for-the-winsnmp-api"></a>Requisitos de software para la API WinSNMP

Una aplicación WinSNMP debe tener acceso a la API WinSNMP a través de la biblioteca de vínculos dinámicos WSNMP32.DLL.

Los siguientes archivos son necesarios para admitir la funcionalidad de la API WinSNMP.



| Nombre de archivo     | Descripción                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| WSNMP32. OBJ  | Biblioteca WinSNMP                                                                              |
| WSNMP32.DLL  | Proporciona la interfaz WinSNMP                                                                   |
| WINSNMP. C    | Archivo de encabezado WinSNMP                                                                          |
| SNMPTRAP.EXE | Recibe capturas de SNMP y las reenvía a MGMTAPI.DLL, la biblioteca de API del administrador SNMP de Microsoft |
| SNMPAPI.DLL  | Proporciona utilidades SNMP                                                                      |



 

 

 




