---
description: Detector de medios (MediaDet)
ms.assetid: 5cdbb6ca-d2c3-4123-b545-198863fed25f
title: Detector de medios (MediaDet)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f34b1dc267480d3d6ea9efe9b9a743623a917b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104157020"
---
# <a name="media-detector-mediadet"></a>Detector de medios (MediaDet)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El objeto de detección de medios (MediaDet) recupera la información de formato y las tramas fijas de los orígenes de archivo. El detector de medios no requiere que funcione el administrador de gráficos de filtro. Para crear este objeto, llame a **CoCreateInstance**. El identificador de clase es CLSID \_ MediaDet.

Para leer archivos de™ de Windows Media, la aplicación debe proporcionar un certificado de software, también denominado clave. Registre la aplicación como un proveedor de claves a través de la interfaz **IObjectWithSite** del detector de medios. Para obtener más información, consulte [desbloquear el SDK de Windows Media Format](unlocking-the-windows-media-format-sdk.md).

El objeto MediaDet expone las siguientes interfaces:

-   [**IMediaDet**](imediadet.md)
-   **IObjectWithSite**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



