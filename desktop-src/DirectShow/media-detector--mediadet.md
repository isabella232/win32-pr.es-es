---
description: Detector de medios (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Detector de medios (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a072a5d70cf392a1b81fc8387d976bea1db2ddaa5ca2328df914be96a791d19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119684975"
---
# <a name="media-detector-mediadet"></a>Detector de medios (MediaDet)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El objeto Media Detector (MediaDet) recupera información de formato y sigue enmarcando los orígenes de archivos. El Detector de medios no requiere que el Administrador de Graph funcione. Para crear este objeto, llame a **CoCreateInstance**. El identificador de clase es CLSID \_ MediaDet.

Para leer Windows archivos ™ multimedia, la aplicación debe proporcionar un certificado de software, también denominado clave. Registre la aplicación como proveedor de claves a través de la **interfaz IObjectWithSite** de Media Detector. Para obtener más información, vea [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md).

El objeto MediaDet expone las interfaces siguientes:

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



