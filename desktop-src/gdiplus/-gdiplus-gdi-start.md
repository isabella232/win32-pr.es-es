---
description: Windows GDI+ es una API basada en clases para programadores de C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e72c8dc87d3dfee22f63fa066ae4c6ae1baf6355fa344448860358e8fd1ad9e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943825"
---
# <a name="gdi"></a>GDI+

## <a name="purpose"></a>Propósito

Windows GDI+ es una API basada en clases para programadores de C/C++. Permite a las aplicaciones usar gráficos y texto con formato tanto en la pantalla de vídeo como en la impresora. Las aplicaciones basadas en la API de Microsoft Win32 no tienen acceso al hardware gráfico directamente. En su lugar, GDI+ interactúa con controladores de dispositivo en nombre de las aplicaciones. GDI+ también es compatible con Microsoft Win64.

## <a name="where-applicable"></a>Donde sea aplicable

GDI+ funciones y clases no se admiten para su uso dentro de Windows servicio. El intento de usar estas funciones y clases desde un servicio Windows puede producir problemas inesperados, como una disminución del rendimiento del servicio y errores o excepciones en tiempo de ejecución.

> [!Note]  
> Al usar la API GDI+, nunca debe permitir que la aplicación descargue fuentes arbitrarias de orígenes que no son de confianza. El sistema operativo requiere privilegios elevados para garantizar que todas las fuentes instaladas sean de confianza.

## <a name="developer-audience"></a>Audiencia de desarrolladores

La GDI+ basada en clases de C++ está diseñada para su uso por parte de programadores de C/C++. Es necesario estar familiarizado Windows interfaz gráfica de usuario y la arquitectura controlada por mensajes.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

GDI+ se puede usar en todas las Windows basadas en aplicaciones. GDI+ se introdujo en Windows XP y Windows Server 2003. Para obtener información sobre qué sistemas operativos deben usar una clase o método determinados, consulte la sección Más información de la documentación de la clase o método.

## <a name="in-this-section"></a>En esta sección

| Tema                                                    | Descripción                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [Información general](-gdiplus-about-gdi--about.md)<br/>     | Información general sobre GDI+.<br/>            |
| [Usando](-gdiplus-using-gdi--use.md)<br/>          | Tareas y ejemplos que usan GDI+.<br/>             |
| [Referencia](-gdiplus-class-gdi-reference.md)<br/> | Documentación de GDI+ API basada en clases de C++.<br/> |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[GDI de Windows](../gdi/windows-gdi.md)
</dt> <dt>

[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> <dt>

[Windows Adquisición de imágenes](../wia/-wia-startpage.md)
</dt> <dt>

[Opengl](../opengl/opengl.md)
</dt> <dt>

[Windows Multimedia](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
