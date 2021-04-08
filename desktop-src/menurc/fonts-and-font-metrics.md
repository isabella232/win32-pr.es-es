---
title: Fuentes y métricas de texto
description: En este tema se describen las fuentes de esquema proporcionadas por Windows, los valores de métricas de fuente que pueden cambiar entre las versiones de Windows y las instrucciones sobre cómo usar las métricas de fuentes en las aplicaciones de escritorio.
ms.assetid: B195154D-0168-4C5E-9CFB-AE7EF63D5F42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27d4eb5f34f5a88e4a0e3e866f9a14784c3895
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995245"
---
# <a name="fonts-and-text-metrics"></a>Fuentes y métricas de texto

En este tema se describen las fuentes de esquema proporcionadas por Windows, los valores de métricas de fuente que pueden cambiar entre las versiones de Windows y las instrucciones sobre cómo usar las métricas de fuentes en las aplicaciones de escritorio.

-   Para obtener información específica de las métricas de fuentes en DirectWrite, vea [métricas de texto](/windows/desktop/DirectWrite/text-metrics).
-   Para obtener más información sobre la administración de texto en aplicaciones con GDI, vea los temas de [fuentes y texto](/windows/desktop/gdi/fonts-and-text).

Para obtener información más detallada sobre el uso de fuentes y las especificaciones de tipo, vea el [sitio de tipografía de Microsoft](https://www.microsoft.com/typography/default.mspx).

## <a name="available-fonts"></a>Fuentes disponibles

Las fuentes de esquema proporcionadas con Windows se entregan como fuentes OpenType con contornos TrueType (Windows también admite fuentes OpenType en el formato CFF). Para ver las listas de todas las fuentes suministradas por Windows, consulte [tipografía de Microsoft: fuentes por producto o familia](https://www.microsoft.com/typography/fonts/default.aspx). Todas las fuentes de esquema de Windows se ajustan a la versión más reciente de la [especificación OpenType](https://www.microsoft.com/typography/otspec/).

Para obtener una lista de todas las fuentes de interfaz de usuario actuales y heredadas, consulte las [métricas de fuentes bloqueadas](#locked-font-metrics) a continuación.

## <a name="font-modifications"></a>Modificaciones de fuentes

Para garantizar la compatibilidad con versiones anteriores, las fuentes rara vez se quitan de Windows. Sin embargo, las fuentes se modifican a menudo. Las modificaciones pueden incluir la adición de caracteres, el redibujo de caracteres existentes, la modificación de sugerencias o la adición o modificación de la compatibilidad con características OpenType avanzadas y el modelado de scripts complejo.

### <a name="locked-font-metrics"></a>Métricas de fuente bloqueadas

Tenga en cuenta que algunos valores asociados a las fuentes de interfaz de usuario y las fuentes predeterminadas usadas en las aplicaciones de Microsoft están bloqueados. Las fuentes de la interfaz de usuario se usan para representar elementos de la interfaz de usuario como leyendas, cuadros de diálogo y menús. Se realizan muy pocos cambios en estas fuentes, dada su alta visibilidad y uso frecuente. Sin embargo, dado que los valores notificados asociados a estas fuentes están bloqueados, puede haber discrepancias entre los valores de fuente notificados y reales.

Los siguientes valores notificados están bloqueados para la interfaz de usuario y las fuentes predeterminadas, y se pueden notificar incorrectamente:

-   Estos valores de la [tabla os/2](https://www.microsoft.com/typography/otspec/os2.htm)de la fuente:
    -   xAvgCharWidth
    -   sTypoLineGap
    -   sTypoAscender
    -   sTypoDescender
    -   usWinAscent
    -   usWinDescent
-   El valor [unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm) establecido en el encabezado de la fuente
-   Valores de la [tabla de métricas de dispositivo vertical (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
-   Ancho de avance de los glifos individuales

Esta es una lista de las fuentes de interfaz de usuario incluidas con Windows 8.1 (que se ven afectadas por valores bloqueados):

| Nombre de script                   | Fuente de la interfaz de usuario               |
|-------------------------------|-----------------------|
| Árabe                        | Segoe UI              |
| Armenio                      | Segoe UI              |
| Bangla (anteriormente bengalí)     | Nirmala UI            |
| Bopomofo                      | Microsoft JhengHei UI |
| Pantallas                       | Segoe UI Symbol       |
| Buginés                      | Leelawadee UI         |
| Canadiense indígena silábico | Gadugi                |
| Cheroqui                      | Gadugi                |
| Copto                        | Segoe UI Symbol       |
| Chino (simplificado)          | Microsoft YaHei UI    |
| Chino (tradicional)         | Microsoft JhengHei UI |
| Cirílico                      | Segoe UI              |
| Devanagari                    | Nirmala UI            |
| Deseret                       | Segoe UI Symbol       |
| Dígito                      | Ebrima                |
| Georgiano                      | Segoe UI              |
| Letra                    | Segoe UI Symbol       |
| Gótico                        | Segoe UI Symbol       |
| Griego                         | Segoe UI              |
| Gujarati                      | Nirmala UI            |
| Gurmukhi                      | Nirmala UI            |
| Hebreo                        | Segoe UI              |
| Cursiva antigua                    | Segoe UI Symbol       |
| Javanés                      | Texto javanés         |
| Japonés                      | Interfaz de usuario de Meiryo             |
| Canarés                       | Interfaz de usuario de Mirmala            |
| Jemer                         | Leelawadee UI         |
| Coreano                        | Malgun Gothic         |
| Lao                           | Leelawadee UI         |
| Latín                         | Segoe UI              |
| Malayalam                     | Nirmala UI            |
| Mongol                     | Mongolian Baiti       |
| Myanmar                       | Myanmar Text          |
| N'Ko                          | Ebrima                |
| Ogham                         | Segoe UI Symbol       |
| OL Chiki                      | Nirmala UI            |
| Turca anterior                    | Segoe UI Symbol       |
| Odia (anteriormente oriya)         | Nirmala UI            |
| Osmanya                       | Ebrima                |
| Phags-pa                      | Microsoft PhagsPa     |
| Rúnica                         | Segoe UI Symbol       |
| Sora Sompeng                  | Nirmala UI            |
| Cingalés                       | Nirmala UI            |
| Siríaco                        | Estrangelo Edessa     |
| Tai le                        | Microsoft Tai Le      |
| Nuevo tai lue moderno                   | Microsoft New Tai Lue |
| Tamil                         | Nirmala UI            |
| Telugu                        | Nirmala UI            |
| Tifinagh                      | Ebrima                |
| Thaana                        | MV Boli               |
| Tailandés                          | Leelawadee UI         |
| Tibetano                       | Microsoft Himalaya    |
| Vai                           | Ebrima                |
| Yi                            | Microsoft Yi Baiti    |



 

Esta es una lista de las fuentes heredadas de la interfaz de usuario que también se ven afectadas por los valores bloqueados:

| Nombre del script (heredado)          | Fuente de la interfaz de usuario (heredada)               |
|-------------------------------|--------------------------------|
| Bangla (anteriormente bengalí)     | Vrinda                         |
| Canadiense indígena silábico | Euphemia                       |
| Cheroqui                      | Plantagenet                    |
| Chino (simplificado)          | Microsoft YaHei y SimSun     |
| Chino (tradicional)         | MingLiU y Microsoft JhengHei |
| Devanagari                    | Mangal                         |
| Idiomas europeos            | Tahoma                         |
| Gujarati                      | Shruti                         |
| Gurmukhi                      | Raavi                          |
| Japonés                      | Interfaz de usuario de Meiryo y MS Gothic        |
| Canarés                       | Tunga                          |
| Jemer                         | Jemer                          |
| Coreano                        | Gulim                          |
| Lao                           | Interfaz de usuario Lao                         |
| Malayalam                     | Kartika                        |
| Idiomas del este de Oriente Medio      | Tahoma                         |
| Odia (anteriormente oriya)         | Kalinga                        |
| Sinhalese                     | Iskoola Pota                   |
| Tamil                         | Torno e Vijaya               |
| Telugu                        | Gautami                        |
| Tailandés                          | Leelawadee y Tahoma          |



 

Estas fuentes se usan como valores predeterminados en las aplicaciones de Microsoft y también se ven afectadas por los valores bloqueados:

-   Arial
-   Calibri
-   Cambria
-   Consolas
-   Courier New
-   MS Mincho
-   Times New Roman
-   Verdana

### <a name="dynamic-font-metrics"></a>Métricas de fuentes dinámicas

Aparte de las métricas bloqueadas mencionadas anteriormente, los valores de fuente se notifican con precisión. Si se cambia una fuente en una nueva versión de Windows, los valores de fuente dinámica serán distintos entre el nuevo y el antiguo. Por ejemplo, cuando se agrega un glifo a una fuente, los valores del encabezado de la fuente pueden cambiar. Podría producirse un recorte si estos valores (entre los que se incluyen xMin, xMax, yMin y yMax y notifican el cuadro de límite mínimo y máximo para los glifos de la fuente) estuviesen bloqueados y no notificaban valores verdaderos.

> [!IMPORTANT]
> Si usa valores de fuente dinámica en la aplicación (como los de [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)), estos valores cambiarán si las fuentes se modifican en versiones futuras de Windows. No use estos valores reales en situaciones en las que el texto debe permanecer estático.

 

## <a name="guidelines-for-using-font-metrics"></a>Directrices para el uso de métricas de fuentes

-   Calcular las métricas de la pantalla y las métricas de fuente (por ejemplo, el ancho medio) cuando se inicia una aplicación y usar estos valores para diseñar la aplicación. Esto proporcionará una representación precisa y coherente, y el diseño responderá a los cambios en las fuentes o aceptará la reserva de fuentes. Para obtener información general sobre la reserva de fuentes y la vinculación de fuentes, consulte [globalización paso a paso: fuentes](https://msdn.microsoft.com/goglobal/bb688134.aspx). Consulte [uso](/windows/desktop/Intl/using-font-fallback) de la reserva de fuentes para obtener información específica de.
    -   Para calcular una métrica base, represente el texto representativo del lenguaje o script deseado.
    -   En el caso de los controles que solo contienen una sola línea de texto sin ajustar, colóquelos para ajustarse al ancho completo del texto sin recortar.
    -   En el caso de los controles con varias líneas, obtenga la longitud total, divida por la longitud de carácter y tiene un ancho sólido con el que trabajar. Tenga en cuenta que esto es complicado en el caso de los scripts complejos donde un solo ' carácter ' al lector puede ser varios puntos de código.
-   Use sTypoAscender, sTypoDescender y unitsPerEm (de la [tabla os/2](https://www.microsoft.com/typography/otspec/os2.htm)) para calcular el espaciado vertical. sTypoAscender se usa para determinar el desplazamiento óptimo desde la parte superior de un marco de texto hasta la primera línea de base y sTypoDescender determina el desplazamiento óptimo desde la parte inferior de un marco de texto hasta la última línea base.
-   Si usa DirectWrite, cree un diseño mediante [**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout). **IDWriteTextLayout** proporciona   +    +  **lineGap** ascendente en el diseño natural. Puede tener acceso a estos valores específicos con las [**\_ \_ métricas de fuente DWRITE**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics). Para obtener información sobre esta interfaz, consulte [formato y diseño de texto](/windows/desktop/DirectWrite/text-formatting-and-layout).
-   Si usa GDI, se representa en OFF Screen y, a continuación, inspecciona el diseño (por ejemplo, la longitud de línea o los caracteres por línea) y vuelve a calcular los parámetros de diseño finales utilizados en la representación real.
-   No cree diseños de forma estática en función de valores concretos para versiones concretas de fuentes. Los valores reales pueden cambiar de una versión a una.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**IDWriteTextLayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**DWRITE \_ \_ métricas de fuente**](/windows/desktop/api/dwrite/ns-dwrite-dwrite_font_metrics)
</dt> <dt>

[**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica)
</dt> <dt>

[unitsPerEm](https://www.microsoft.com/typography/otspec/head.htm)
</dt> <dt>

[SO/2 tabla](https://www.microsoft.com/typography/otspec/os2.htm)
</dt> <dt>

[Tabla de métricas de dispositivo vertical (VDMX)](https://www.microsoft.com/typography/otspec/vdmx.htm)
</dt> <dt>

[Tipografía de Microsoft: fuentes por producto o familia](https://www.microsoft.com/typography/fonts/default.aspx)
</dt> <dt>

**Vista**
</dt> <dt>

[Métricas de texto (DirectWrite)](/windows/desktop/DirectWrite/text-metrics)
</dt> <dt>

[Fuentes y texto (GDI)](/windows/desktop/gdi/fonts-and-text)
</dt> <dt>

[Tipografía de Microsoft](https://www.microsoft.com/typography/default.mspx)
</dt> </dl>

 

 