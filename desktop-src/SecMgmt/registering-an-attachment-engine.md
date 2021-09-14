---
description: Para que el motor de configuración de seguridad pueda llamar al motor de datos adjuntos para procesar tareas específicas del servicio, debe instalar el motor de datos adjuntos y registrarlo con el motor de configuración de seguridad.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registro de un motor de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071129"
---
# <a name="registering-an-attachment-engine"></a>Registro de un motor de datos adjuntos

Para que el motor de configuración de seguridad pueda llamar al motor de datos adjuntos para procesar tareas específicas del servicio, debe instalar el motor de datos adjuntos y registrarlo con el motor de configuración de seguridad.

**Para instalar y registrar el archivo DLL del motor de datos adjuntos**

1.  Copie el archivo DLL del motor de datos adjuntos en un directorio del sistema. El directorio preferido es %windir% \\ secedit \\ attachments. Si este directorio no existe, debe crearlo.
2.  Cree una clave del Registro en el nodo siguiente. El *nombre del servicio* es el nombre registrado de los datos adjuntos y debe ser el mismo nombre de servicio que se usa en Service Control Manager, un módulo que administra la detención e inicio de los servicios. El nombre también debe ser único para que no entre en conflicto con los nombres de otros datos adjuntos.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Cree el siguiente valor de cadena en la nueva clave del Registro. *ruta de acceso del motor de* datos adjuntos es la ruta de acceso completa al módulo del motor de datos adjuntos.<dl> <dd>**ServiceAttachmentPath**  =  *ruta de acceso del motor de datos adjuntos*<dl> <dt>

Tipo de datos
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



