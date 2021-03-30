---
title: Uso de extensiones de NPS
description: Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS).
ms.assetid: 3ee16279-7e11-4587-ae43-f0296b7e7594
ms.tgt_platform: multiple
keywords:
- Servicio de autenticación de Internet IAS, tareas
- Servicio de autenticación de Internet IAS, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a1cc9f10c810ec9fe16618144db11686a1e2132
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2020
ms.locfileid: "104533064"
---
# <a name="using-nps-extensions"></a>Uso de extensiones de NPS

Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) al servidor de directivas de redes (NPS). El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

* * Windows Server 2008 R2 y Windows Server 2008: * *

Los ejemplos de acceso telefónico y Nombredemapa amplían la funcionalidad de NPS.



| Muestra             | Descripción                                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Omiten<br/>  | En este ejemplo se implementa un archivo DLL de extensión RADIUS que comprueba el bit de marcado del usuario.<br/>                                                                                                              |
| nombreDeMapa<br/> | Este archivo DLL de extensión de ejemplo busca la cuenta designada en todos los dominios de confianza. Esto permite autenticar a los usuarios de varios dominios sin que los usuarios tengan que proporcionar su nombre de dominio.<br/> |



 

Puede encontrar el código fuente de las aplicaciones de ejemplo Nombredemapa y Dialen en la lista siguiente. *Ubicación*,% install Path%, designa el directorio de instalación base para equipos x64. Vea también [Kit de desarrollo de software (SDK) de Windows para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk), kit de desarrollo de software (SDK) de Microsoft Windows y [descargas para el desarrollo de aplicaciones de la tienda Windows](https://msdn.microsoft.com/windows/apps/br229516).

<dl> <dt>

Windows SDK para Windows 8
</dt> <dd>

Windows Server 2012

Vínculo de descarga: N/A

Nombredemapa: no

Marcado: no

Ubicación: N/A

</dd> <dt>

Kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0
</dt> <dd>

Windows Server 2008 R2

Vínculo de descarga: <https://www.microsoft.com/download/en/confirmation.aspx?id=8279>

Nombredemapa: sí

Marcado: no

Ubicación:% install path% \\ Microsoft SDKs \\ Windows \\ v 7.1 \\ Samples \\ netds \\ IAS

</dd> <dt>

Windows SDK
</dt> <dd>

Windows Server 2008

Vínculo de descarga: <https://www.microsoft.com/download/details.aspx?id=5023>

Nombredemapa: sí

Marcado: no

Ubicación:% install path% \\ Microsoft SDKs \\ Windows \\ v 6.1 \\ Samples \\ NetDs \\ IAS

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descargas para desarrolladores](https://msdn.microsoft.com/windows/apps/br229516)
</dt> <dt>

[Windows SDK para Windows 8](https://developer.microsoft.com/windows/downloads/windows-8-sdk)
</dt> </dl>

 

 





