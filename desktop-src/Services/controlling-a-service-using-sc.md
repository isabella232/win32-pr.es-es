---
description: El WINDOWS SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede usar para controlar un servicio. Sus comandos corresponden a las funciones proporcionadas por el SCM. La sintaxis es la siguiente.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controlar un servicio mediante SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265071"
---
# <a name="controlling-a-service-using-sc"></a>Controlar un servicio mediante SC

El WINDOWS SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede usar para controlar un servicio. Sus comandos corresponden a las funciones proporcionadas por el SCM. La sintaxis es la siguiente.

## <a name="syntax"></a>Sintaxis

**sc** \[ *ServerName* \] *Comando* \[ *ServiceName* \] \[ *option1* \] \[ *option2* \] ...

<dl> <dt>

<span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nombredeservidor*
</dt> <dd>

Nombre de servidor opcional. Use el formato \\ \\ *NombreDeServidor*.

</dd> <dt>

<span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Comando*
</dt> <dd>

Uno de los siguientes comandos:

<dl> <dd>continue</dd> <dd>control</dd> <dd>Interrogar</dd> <dd>pause</dd> <dd>start</dd> <dd>stop</dd> </dl> </dd> <dt>

<span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*Servicename*
</dt> <dd>

Nombre del servicio, tal como se especificó cuando se instaló.

</dd> <dt>

<span id="option1"></span><span id="OPTION1"></span>*option1*
</dt> <dd>

Parámetro opcional.

</dd> <dt>

<span id="option2"></span><span id="OPTION2"></span>*option2*
</dt> <dd>

Parámetro opcional.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para ver la sintaxis completa de un comando, use el siguiente comando:

**sc** *(Comando)*

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Solicitudes de control de servicio](service-control-requests.md)
</dt> <dt>

[Inicio del servicio](service-startup.md)
</dt> </dl>

 

 



