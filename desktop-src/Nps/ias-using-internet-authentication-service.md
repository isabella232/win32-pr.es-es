---
title: Uso de extensiones NPS
description: Obtenga información sobre el uso de extensiones NPS. El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS del servicio de autenticación de Internet, tareas
- IAS del servicio de autenticación de Internet , mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db3590ed10ec77e57c86bfad3e0e0b1160e70a2d6fcc08abc911a14614543f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074305"
---
# <a name="using-nps-extensions"></a>Uso de extensiones NPS

El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS). El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

**Windows Server 2008 R2 y Windows Server 2008: **

Los ejemplos de DialIn y MapName amplían la funcionalidad nps.



| Muestra             | Descripción                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialIn<br/>  | En este ejemplo se implementa un archivo DLL de extensión RADIUS que comprueba el bit de acceso telefónico del usuario.<br/>                                                                                                              |
| nombreDeMapa<br/> | Este archivo DLL de extensión de ejemplo busca en todos los dominios de confianza la cuenta designada. Esto permite que los usuarios de varios dominios se autentiquen sin que los usuarios tengan que proporcionar su nombre de dominio.<br/> |



 

Puede encontrar el código fuente de las aplicaciones de ejemplo MapName y DialIn en la lista siguiente. *Ubicación*, %Ruta de instalación%, designa el directorio de instalación base para equipos x64. Consulte también [Windows Software Development Kit (SDK) for Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), Microsoft Windows Software Development Kit (SDK) y Downloads for Windows Store app [development](https://msdn.microsoft.com/windows/apps/br229516).

<dl> <dt>

Windows SDK para Windows 8
</dt> <dd>

Windows Server 2012

Vínculo de descarga: N/A

MapName: No

DialIn: No

Ubicación: N/A

</dd> <dt>

Kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4.0
</dt> <dd>

Windows Server 2008 R2

Vínculo de descarga: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName: Sí

DialIn: No

Ubicación: %Ruta de instalación% SDK de \\ Microsoft \\ Windows \\ v7.1 \\ Ejemplos \\ netds \\ ias

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

Vínculo de descarga: <https://www.microsoft.com/download/details.aspx?id=5023>

MapName: Sí

DialIn: No

Ubicación: %Ruta de instalación% SDK de \\ Microsoft \\ Windows \\ \\ \\ iAS de netD de ejemplo v6.1 \\

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descargas para desarrolladores](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





