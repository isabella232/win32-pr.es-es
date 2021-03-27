---
description: Windows GDI+ es una API basada en clases para los programadores de C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154221"
---
# <a name="gdi"></a>GDI+

## <a name="purpose"></a>Propósito

Windows GDI+ es una API basada en clases para los programadores de C/C++. Permite a las aplicaciones utilizar gráficos y texto con formato tanto en la pantalla de vídeo como en la impresora. Las aplicaciones basadas en la API de Microsoft Win32 no tienen acceso al hardware gráfico directamente. En su lugar, GDI+ interactúa con controladores de dispositivo en nombre de las aplicaciones. GDI+ también es compatible con Microsoft Win64.

## <a name="where-applicable"></a>Donde sea aplicable

Las funciones y clases GDI+ no se admiten para su uso en un servicio de Windows. El intento de usar estas funciones y clases de un servicio de Windows puede producir problemas inesperados, como el rendimiento reducido del servicio y las excepciones o errores en tiempo de ejecución.

> [!Note]  
> Cuando se usa la API GDI+, nunca se debe permitir que la aplicación Descargue fuentes arbitrarias de orígenes que no son de confianza. El sistema operativo requiere privilegios elevados para asegurarse de que todas las fuentes instaladas son de confianza.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La interfaz basada en clases de C++ de GDI+ está diseñada para que la utilicen los programadores de C/C++. Es necesario estar familiarizado con la interfaz gráfica de usuario de Windows y la arquitectura controlada por mensajes.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

GDI+ se puede usar en todas las aplicaciones basadas en Windows. GDI+ se presentó en Windows XP y Windows Server 2003. Para obtener información sobre los sistemas operativos necesarios para usar una clase o un método determinados, vea la sección más información de la documentación de la clase o el método.

## <a name="in-this-section"></a>En esta sección

| Tema                                                    | Descripción                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [Información general](-gdiplus-about-gdi--about.md)<br/>     | Información general sobre GDI+.<br/>            |
| [Utilizan](-gdiplus-using-gdi--use.md)<br/>          | Tareas y ejemplos con GDI+.<br/>             |
| [Referencia](-gdiplus-class-gdi-reference.md)<br/> | Documentación de la API basada en clases de C++ de GDI+.<br/> |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[GDI de Windows](../gdi/windows-gdi.md)
</dt> <dt>

[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> <dt>

[Adquisición de imágenes de Windows](../wia/-wia-startpage.md)
</dt> <dt>

[OpenGL](../opengl/opengl.md)
</dt> <dt>

[Multimedia de Windows](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
