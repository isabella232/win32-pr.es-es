---
description: El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede utilizar para controlar un servicio. Sus comandos se corresponden con las funciones proporcionadas por el SCM. La sintaxis es la siguiente.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controlar un servicio mediante SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668295"
---
# <a name="controlling-a-service-using-sc"></a>Controlar un servicio mediante SC

El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede utilizar para controlar un servicio. Sus comandos se corresponden con las funciones proporcionadas por el SCM. La sintaxis es la siguiente.

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

<dl> <dd>continue</dd> <dd>control</dd> <dd>interrogar</dd> <dd>pause</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

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

[Solicitudes de control de servicio](service-control-requests.md)
</dt> <dt>

[Inicio del servicio](service-startup.md)
</dt> </dl>

 

 



