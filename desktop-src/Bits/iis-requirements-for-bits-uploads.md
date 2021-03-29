---
title: Requisitos de IIS para cargas de BITS
description: En el caso de las cargas, BITS requiere IIS 6,0 en Windows Server 2003 y IIS 7,0 en Windows Server 2008; BITS no admite IIS 5,1 en Windows XP.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773656"
---
# <a name="iis-requirements-for-bits-uploads"></a>Requisitos de IIS para cargas de BITS

En el caso de las cargas, BITS requiere IIS 6,0 en Windows Server 2003 y IIS 7,0 en Windows Server 2008; BITS no admite IIS 5,1 en Windows XP. El directorio virtual de IIS debe estar habilitado para cargas y tener las extensiones de IIS de BITS configuradas.

**Instalaciones básicas de Windows Server:** No se admiten las extensiones de IIS de BITS.

En Windows Server 2008, use el **Administrador del servidor** para instalar la característica extensiones de servidor bits. En **Administrador del servidor**, haga clic en **características** en el panel izquierdo. En el **Asistente para agregar características**, compruebe extensiones de servidor bits. Tenga en cuenta que los roles de compatibilidad con la administración de IIS 6 deben estar instalados.

En Windows Server 2003, use el **Asistente para componentes de Windows** para instalar la extensión de servidor bits. En el **Panel de control**, seleccione **Agregar o quitar programas**. A continuación, seleccione **Agregar o quitar componentes de Windows** para mostrar el **Asistente para componentes de Windows**. La extensión de servidor BITS es un subcomponente de Internet Information Services (IIS), que es un subcomponente del servidor de aplicaciones Web.

> [!Note]  
> Si se reinicia el servicio IISAdmin, el proceso de trabajo de IIS se debe reciclar antes de que el servicio BITS pueda reanudar las cargas. El proceso de trabajo de IIS se puede reciclar manualmente mediante la utilidad de línea de comandos **IISReset.exe** .

 

Para obtener información sobre cómo configurar IIS para cargas, consulte [configuración del servidor para cargas](setting-up-the-server-for-uploads.md).

Para obtener más información sobre las propiedades que BITS agrega a IIS, consulte [configuración del servidor bits para trabajos de carga](bits-server-settings-for-upload-jobs.md).

 

 




