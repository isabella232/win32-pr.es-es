---
description: Escala de tiempo
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688732"
---
# <a name="timeline"></a>Escala de tiempo

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El objeto Timeline administra todos los objetos de un proyecto de edición de vídeo. Para crear este objeto, llame a **CoCreateInstance**. El identificador de clase es CLSID \_ AMTimeline.

Para leer archivos de™ de Windows Media, la aplicación debe proporcionar un certificado de software, también denominado clave. Registre la aplicación como proveedor de claves a través de la interfaz **IObjectWithSite** de la escala de tiempo. Para obtener más información, consulte [desbloquear el SDK de Windows Media Format](unlocking-the-windows-media-format-sdk.md).

El objeto Timeline expone las siguientes interfaces:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Modelo de escala de tiempo](the-timeline-model.md)
</dt> <dt>

[Construir una escala de tiempo](constructing-a-timeline.md)
</dt> </dl>

 

 



