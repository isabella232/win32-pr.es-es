---
description: Antes de que el motor de configuración de seguridad pueda llamar a su motor de datos adjuntos para procesar tareas específicas del servicio, debe instalar el motor de datos adjuntos y registrarlo en el motor de configuración de seguridad.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrar un motor de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686677"
---
# <a name="registering-an-attachment-engine"></a>Registrar un motor de datos adjuntos

Antes de que el motor de configuración de seguridad pueda llamar a su motor de datos adjuntos para procesar tareas específicas del servicio, debe instalar el motor de datos adjuntos y registrarlo en el motor de configuración de seguridad.

**Para instalar y registrar la DLL del motor de datos adjuntos**

1.  Copie el archivo DLL del motor de datos adjuntos en un directorio del sistema. El directorio preferido es% WINDIR% \\ secedit \\ Attachments. Si este directorio no existe, debe crearlo.
2.  Cree una clave del registro en el siguiente nodo. El *nombre del servicio* es el nombre registrado para los datos adjuntos y debe ser el mismo nombre de servicio usado en el administrador de control de servicios, un módulo que administra la detención e inicio de los servicios. El nombre también debe ser único, por lo que no entra en conflicto con los nombres de otros datos adjuntos.

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  Cree el siguiente valor de cadena en la nueva clave del registro. *ruta del motor de datos adjuntos* es la ruta de acceso completa al módulo del motor de datos adjuntos.<dl> <dd>**ServiceAttachmentPath**  =  *ruta del motor de datos adjuntos*<dl> <dt>

Tipo de datos
</dt> <dd>REG_SZ</dd> </dl> </dd> </dl>

 

 



