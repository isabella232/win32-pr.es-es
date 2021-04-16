---
title: Jerarquía de clases de objeto Winnt
description: La jerarquía de clases de objeto WinNT se inicia desde el objeto de espacio de nombres.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- Editor de servicios de WinNT ADSI, jerarquía de clases de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531834"
---
# <a name="winnt-object-class-hierarchy"></a>Jerarquía de clases de objeto Winnt

La jerarquía de clases de objeto WinNT se inicia desde el objeto de espacio de nombres.



| Object (clase)                   | Descripción                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Espacio de nombres<br/>           | Contenedor de objetos de nivel superior.<br/>                                            |
| Domain<br/>              | Dominio de Windows NT.<br/>                                                 |
| User (Usuario)<br/>                | Cuenta de usuario.<br/>                                                          |
| Grupo<br/>               | Cuenta de grupo para administrar derechos de acceso.<br/>                              |
| UserGroupCollection<br/> | Conjunto de grupos de usuarios que implementan [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/>  |
| GroupCollection<br/>     | Un conjunto de otros grupos que implementan [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/> |
| Computer<br/>            | Windows NT 4,0 Server o Workstation.<br/>                                  |
| PrintJob<br/>            | Trabajo de impresión en la cola de impresión.<br/>                                          |
| PrintJobsCollection<br/> | Un conjunto de trabajos de impresión.<br/>                                                   |
| PrintQueue<br/>          | Cola de impresión en un administrador de trabajos de impresión.<br/>                                      |
| Servicio<br/>             | Aplicación que se ejecuta como un servicio.<br/>                                      |
| FileService<br/>         | Servicios que acceden al sistema de archivos.<br/>                                        |
| FileShare<br/>           | Punto de recurso compartido de archivos.<br/>                                                      |
| Recurso<br/>            | Un recurso en el servicio.<br/>                                             |
| Sesión<br/>             | Una conexión de servicio de archivos activa.<br/>                                     |
| User (Usuario)<br/>                | Cuenta de usuario local.<br/>                                                    |
| Grupo<br/>               | Grupo local.<br/>                                                           |
| UserCollection<br/>      | Colección de usuarios locales.<br/>                                             |
| GroupCollection<br/>     | Colección de grupos locales.<br/>                                            |
| Schema<br/>              | Contenedor de esquemas de Winnt.<br/>                                                |
| Clase<br/>               | Definición de clase de esquema.<br/>                                               |
| Propiedad<br/>            | Definición de atributo de esquema.<br/>                                           |
| Sintaxis<br/>              | Sintaxis de una propiedad.<br/>                                                  |



 

 

 





