---
title: Requisitos de IIS para cargas de BITS
description: Para las cargas, BITS requiere IIS 6.0 en Windows Server 2003 e IIS 7.0 en Windows Server 2008; BITS no admite IIS 5.1 en Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974642"
---
# <a name="iis-requirements-for-bits-uploads"></a>Requisitos de IIS para cargas de BITS

Para las cargas, BITS requiere IIS 6.0 en Windows Server 2003 e IIS 7.0 en Windows Server 2008; BITS no admite IIS 5.1 en Windows XP. El directorio virtual de IIS debe estar habilitado para las cargas y tener configuradas las extensiones DE IIS de BITS.

**Instalaciones principales de Windows Server:** No se admiten las extensiones IIS de BITS.

En Windows Server 2008, use la Administrador del servidor **para** instalar la característica extensiones de servidor BITS. En **Administrador del servidor**, haga clic **en Características** en el panel izquierdo. En el **Asistente para agregar características,** active Extensiones de servidor BITS. Tenga en cuenta que deben instalarse los roles de compatibilidad de administración de IIS 6.

En Windows Server 2003, use el Asistente **para componentes** de Windows para instalar la extensión de servidor BITS. En **Panel de control**, seleccione **Agregar o quitar programas.** A continuación, **seleccione Agregar o quitar Windows componentes para** mostrar el Asistente para Windows **componentes.** La extensión de servidor BITS es un subcomponente de Internet Information Services (IIS) que es un subcomponente del servidor de aplicaciones web.

> [!Note]  
> Si se reinicia el servicio IISAdmin, el proceso de trabajo de IIS debe reciclarse antes de que el servicio BITS pueda reanudar las cargas. El proceso de trabajo de IIS se puede reciclar manualmente mediante la utilidad **IISReset.exe** línea de comandos.

 

Para obtener información sobre cómo configurar IIS para cargas, vea [Configurar el servidor para cargas](setting-up-the-server-for-uploads.md).

Para obtener más información sobre las propiedades que BITS agrega a IIS, vea [Bits Server Configuración for Upload Jobs](bits-server-settings-for-upload-jobs.md).

 

 




