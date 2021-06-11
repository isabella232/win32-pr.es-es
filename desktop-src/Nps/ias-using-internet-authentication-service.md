---
title: Uso de extensiones NPS
description: Obtenga información sobre el uso de extensiones NPS. El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- IAS del servicio de autenticación de Internet, tareas
- Internet Authentication Service IAS , mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f422c005d6810a4035450e24de1324b28361f1
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989081"
---
# <a name="using-nps-extensions"></a>Uso de extensiones NPS

El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS). El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

**Windows Server 2008 R2 y Windows Server 2008: **

Los ejemplos de DialIn y MapName amplían la funcionalidad nps.



| Muestra             | Descripción                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialIn<br/>  | En este ejemplo se implementa un archivo DLL de extensión RADIUS que comprueba el bit de acceso telefónico del usuario.<br/>                                                                                                              |
| nombreDeMapa<br/> | Este archivo DLL de extensión de ejemplo busca en todos los dominios de confianza la cuenta designada. Esto permite que los usuarios de varios dominios se autentiquen sin que los usuarios tengan que proporcionar su nombre de dominio.<br/> |



 

Puede encontrar el código fuente de las aplicaciones de ejemplo MapName y DialIn en la lista siguiente. *Ubicación*, %Ruta de instalación%, designa el directorio de instalación base para equipos x64. Consulte también [Kit de desarrollo de software de Windows (SDK)](https://developer.microsoft.com/windows/downloads/windows-8-sdk)para Windows 8 , Microsoft Kit de desarrollo de software de Windows (SDK) y Descargas para el desarrollo de [aplicaciones de la Tienda Windows.](https://msdn.microsoft.com/windows/apps/br229516)

<dl> <dt>

Windows SDK para Windows 8
</dt> <dd>

Windows Server 2012

Vínculo de descarga: N/A

MapName: No

DialIn: No

Ubicación: N/A

</dd> <dt>

Microsoft Kit de desarrollo de software de Windows (SDK) para Windows 7 y .NET Framework 4.0
</dt> <dd>

Windows Server 2008 R2

Vínculo de descarga: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

MapName: Sí

DialIn: No

Ubicación: %Ruta de instalación% \\ SDK de Microsoft Windows \\ \\ v7.1 \\ Ejemplos \\ netds \\ ias

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

Vínculo de descarga: <https://www.microsoft.com/download/details.aspx?id=5023>

MapName: Sí

DialIn: No

Ubicación: %Install Path% \\ Microsoft SDKs \\ Windows \\ v6.1 \\ Samples \\ NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descargas para desarrolladores](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





