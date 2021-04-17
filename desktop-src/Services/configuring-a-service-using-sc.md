---
description: El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede usar para consultar o modificar la base de datos de los servicios instalados. Sus comandos se corresponden con las funciones proporcionadas por el SCM. La sintaxis es la siguiente.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configuración de un servicio mediante SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666348"
---
# <a name="configuring-a-service-using-sc"></a>Configuración de un servicio mediante SC

El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede usar para consultar o modificar la base de datos de los servicios instalados. Sus comandos se corresponden con las funciones proporcionadas por el SCM. La sintaxis es la siguiente.

## <a name="syntax"></a>Sintaxis

**SC** \[ *NombreDeServidor* \] *Comando* \[  \] ServiceName \[  \] Opción1 \[ *opción2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*
</dt> <dd>

Nombre de servidor opcional. Use el formato \\ \\ *ServerName*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*
</dt> <dd>

Uno de los siguientes comandos:

<dl> <dd>boot</dd> <dd>config</dd> <dd>create</dd> <dd>delete</dd> <dd>description</dd> <dd>EnumDepend</dd> <dd>failure</dd> <dd>failureflag</dd> <dd>GetDisplayName</dd> <dd>GetKeyName</dd> <dd>Lock</dd> <dd>qc</dd> <dd>qdescription</dd> <dd>qfailure</dd> <dd>qfailureflag</dd> <dd>qprivs</dd> <dd>qsidtype</dd> <dd>Query</dd> <dd>QueryEx</dd> <dd>priv</dd> <dd>QueryLock</dd> <dd>sdset</dd> <dd>sdshow</dd> <dd>showsid</dd> <dd>SID</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*
</dt> <dd>

Nombre del servicio, tal y como se especificó cuando se instaló.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*Opción1*
</dt> <dd>

Parámetro opcional.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*opción2*
</dt> <dd>

Parámetro opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para ver la sintaxis completa de un comando, use el siguiente comando:

**SC** ( *comando* )

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de servicio](service-configuration.md)
</dt> <dt>

[Instalación, eliminación y enumeración del servicio](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



