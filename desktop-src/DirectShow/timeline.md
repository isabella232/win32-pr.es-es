---
description: Escala de tiempo
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891644"
---
# <a name="timeline"></a>Escala de tiempo

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El objeto de escala de tiempo administra todos los objetos de un proyecto de edición de vídeo. Para crear este objeto, llame a **CoCreateInstance**. El identificador de clase es CLSID \_ AMTimeline.

Para leer Windows archivos multimedia™, la aplicación debe proporcionar un certificado de software, también denominado clave. Registre la aplicación como proveedor de claves a través de la **interfaz IObjectWithSite** de la escala de tiempo. Para obtener más información, vea [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md)(Desbloquear el SDK Windows media format ).

El objeto timeline expone las interfaces siguientes:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **Ipersiststream**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de escala de tiempo](the-timeline-model.md)
</dt> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



