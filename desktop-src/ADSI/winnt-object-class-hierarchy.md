---
title: Jerarquía de clases de objetos WinNT
description: La jerarquía de clases de objetos WinNT se inicia desde el objeto Namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- AdsI del proveedor de servicios WinNT , jerarquía de clases de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e893839393ad3b9aaa42557d90f9bf279ab0625e1225ab41f2d1a3c7e7980a1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589765"
---
# <a name="winnt-object-class-hierarchy"></a>Jerarquía de clases de objetos WinNT

La jerarquía de clases de objetos WinNT se inicia desde el objeto Namespace.



| Object (clase)                   | Descripción                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Espacio de nombres<br/>           | Contenedor de objetos de nivel superior.<br/>                                            |
| Domain<br/>              | Dominio Windows NT.<br/>                                                 |
| Usuario<br/>                | Cuenta de usuario.<br/>                                                          |
| Grupo<br/>               | Cuenta de grupo para administrar los derechos de acceso.<br/>                              |
| UserGroupCollection<br/> | Conjunto de grupos de usuarios que implementan [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/>  |
| GroupCollection<br/>     | Un conjunto de otros grupos que implementan [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/> |
| Computer<br/>            | Windows Servidor o estación de trabajo NT 4.0.<br/>                                  |
| Printjob<br/>            | Trabajo de impresión en la cola de impresión.<br/>                                          |
| PrintJobsCollection<br/> | Un conjunto de trabajos de impresión.<br/>                                                   |
| PrintQueue<br/>          | Cola de impresión en un administrador de trabajos de impresión.<br/>                                      |
| Servicio<br/>             | Aplicación que se ejecuta como servicio.<br/>                                      |
| FileService<br/>         | Servicios que acceden al sistema de archivos.<br/>                                        |
| FileShare<br/>           | Punto de recurso compartido de archivos.<br/>                                                      |
| Recurso<br/>            | Un recurso del servicio.<br/>                                             |
| Sesión<br/>             | Una conexión de servicio de archivos activa.<br/>                                     |
| Usuario<br/>                | Cuenta de usuario local.<br/>                                                    |
| Grupo<br/>               | Grupo local.<br/>                                                           |
| UserCollection<br/>      | Colección de usuarios locales.<br/>                                             |
| GroupCollection<br/>     | Colección de grupos locales.<br/>                                            |
| Schema<br/>              | Contenedor de esquema WinNT.<br/>                                                |
| Clase<br/>               | Definición de clase de esquema.<br/>                                               |
| Propiedad<br/>            | Definición de atributo de esquema.<br/>                                           |
| Syntax<br/>              | Sintaxis de una propiedad.<br/>                                                  |



 

 

 





