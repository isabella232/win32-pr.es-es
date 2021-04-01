---
title: Direct2D y High-PPP
description: Describe la forma en que Direct2D acomoda la visualización de PPP alta.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, alta PPP
- alta PPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995574"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D y High-PPP

Escribir una aplicación compatible con PPP es la clave para que una interfaz de usuario (UI) tenga un aspecto coherente en una amplia variedad de valores de pantalla de alta ppp. Una aplicación que no sea compatible con PPP pero que se esté ejecutando en una configuración de pantalla de valores altos de PPP puede verse afectada por muchos artefactos visuales, incluidos el escalado incorrecto de los elementos de la interfaz de usuario, el texto recortado y las imágenes borrosas. Al agregar compatibilidad en la aplicación para el reconocimiento de PPP, se hace que la presentación de la interfaz de usuario de la aplicación sea más predecible, lo que hace que sea más atractiva y fácil de leer para los usuarios. Afortunadamente, Direct2D facilita más que nunca la escritura de aplicaciones que funcionan bien en un valor alto de PPP. En este tema se incluyen las siguientes secciones.

-   [Compatibilidad con alto nivel de PPP en Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 y alta PPP](#windows-8-and-high-dpi)
-   [¿Qué es una DIP?](#what-is-a-dip)
-   [Temas relacionados](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Compatibilidad con alto nivel de PPP en Direct2D

Direct2D proporciona las siguientes características para trabajar con escenarios de alta PPP:

-   Respeta automáticamente el valor de PPP del sistema al crear un destino de representación en ventanas, siempre y cuando el manifiesto de aplicación indique que la aplicación controla el valor de PPP correctamente. (Para obtener información sobre cómo declarar que la aplicación tiene reconocimiento de PPP, consulte [Cómo asegurarse de que la aplicación se muestra correctamente en pantallas de alta PPP](how-to--size-a-window-properly-for-high-dpi-displays.md)).
-   Expresa las coordenadas en DIP (píxeles independientes del dispositivo), lo que permite que la aplicación se escale automáticamente cuando cambie la configuración de PPP.
-   Permite que los mapas de bits tengan un PPP y los escala correctamente tomando en cuenta los ppp. Esta característica también se puede usar para mantener iconos en diferentes resoluciones.
-   Expresa la mayoría de los recursos en DIP, lo que hace que los recursos sean independientes de la resolución.
-   Utiliza un espacio de coordenadas de punto flotante y un suavizado de contorno, por lo que cualquier contenido se puede escalar a cualquier PPP arbitrario.

La canalización de gráficos de Direct2D está diseñada para escalar de 96 PPP a 1200DPI.

## <a name="windows-8-and-high-dpi"></a>Windows 8 y alta PPP

A partir de Windows 8, hay características adicionales para la compatibilidad con alta calidad de PPP.

Si el PPP del contexto del dispositivo es suficientemente alto, Direct2D cambia el umbral que usa para habilitar el suavizado de contorno vertical del texto. Esto da como resultado una representación de texto más rápida en pantallas de alta ppp. Además, puede cambiar el modo de unidad a píxeles en lugar de a DIP mediante el método [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) . Si establece el modo de unidad en píxeles y el valor de PPP del contexto del dispositivo en el valor de PPP de la pantalla, la optimización sigue estando habilitada.

## <a name="what-is-a-dip"></a>¿Qué es una DIP?

Un píxel independiente del dispositivo (DIP) es un píxel lógico que se asigna a los píxeles del dispositivo físico a través de un escalar, el valor de PPP. PPP significa puntos por pulgada, donde un punto representa un píxel de dispositivo físico. (La nomenclatura procede de la impresión, donde los puntos son el punto de tinta más pequeño que puede producir un proceso de impresión). Dado que un monitor estándar solía tener 96 puntos por pulgada, un DPI de 96 significaba que un píxel independiente del dispositivo (o DIP) asigna 1:1 con un píxel físico. Por ejemplo, si los PPP fueran 96 \* 2 = 192, una sola DIP abarcaría dos píxeles físicos.

Hay muchas razones por las que las aplicaciones no controlan necesariamente este ajuste de escala correctamente; uno de los motivos más sencillos es que requiere un trabajo adicional para detectar y usar este valor escalar cuando se representa. En Direct2D, el escalado se aplica de forma predeterminada. Debido a esta asignación, los píxeles del dispositivo físico pueden acabar en coordenadas DIP fraccionarias, que es uno de los motivos por los que Direct2D usa un espacio de coordenadas de punto flotante.

<dl> píxel físico = (DIP × PPP)/96  
</dl>

Para convertir un píxel físico en una DIP, use esta fórmula:

<dl> DIP = (píxel físico × 96)/PPP  
</dl>

> [!Note]
>
> A partir de Windows 8, puede cambiar el modo de unidad a píxeles en lugar de a DIP mediante el método [**ID2D1DeviceContext:: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo asegurarse de que la aplicación se muestre correctamente en pantallas de alta resolución de PPP](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 