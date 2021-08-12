---
description: Escala de tiempo
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Escala de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85809aed689d63ccdfc0b1dee1b5b792cafc9d7d0267d27e33bd7b6c1bea6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651260"
---
# <a name="timeline"></a>Escala de tiempo

> [!Note]  
> \[En desuso. Esta API puede quitarse de futuras versiones de Windows.\]

 

El objeto de escala de tiempo administra todos los objetos de un proyecto de edición de vídeo. Para crear este objeto, llame a **CoCreateInstance**. El identificador de clase es CLSID \_ AMTimeline.

Para leer Windows archivos ™ multimedia, la aplicación debe proporcionar un certificado de software, también denominado clave. Registre la aplicación como proveedor de claves a través de la **interfaz IObjectWithSite** de la escala de tiempo. Para obtener más información, vea [Unlocking the Windows Media Format SDK](unlocking-the-windows-media-format-sdk.md)( Desbloqueo del SDK de formato multimedia).

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

 

 



