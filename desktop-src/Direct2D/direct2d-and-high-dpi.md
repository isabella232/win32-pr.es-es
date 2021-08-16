---
title: Direct2D y valores altos de PPP
description: Describe cómo Direct2D se adapta a la pantalla de valores altos de PPP.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, valores altos de PPP
- valores altos de PPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5c48f9a1b3552115ebbec8a54a6878716ef34675e41193ae08fb9cb8e55bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825988"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D y valores altos de PPP

Escribir una aplicación compatible con PPP es la clave para que una interfaz de usuario (UI) tenga un aspecto coherente en una amplia variedad de configuraciones de pantalla de valores altos de PPP. Una aplicación que no tiene reconocimiento de PPP pero que se ejecuta en una configuración de pantalla de valores altos de PPP puede sufrir muchos artefactos visuales, incluido el escalado incorrecto de elementos de la interfaz de usuario, el texto recortado y las imágenes desenfoque. Al agregar compatibilidad en la aplicación para el reconocimiento de PPP, hace que la presentación de la interfaz de usuario de la aplicación sea más predecible, lo que hace que sea más atractiva visualmente y más fácil de leer para los usuarios. Afortunadamente, Direct2D facilita que nunca escribir aplicaciones que funcionen bien con valores altos de PPP. En este tema se incluyen las siguientes secciones.

-   [Compatibilidad con valores altos de PPP en Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 y valores altos de PPP](#windows-8-and-high-dpi)
-   [¿Qué es una DIP?](#what-is-a-dip)
-   [Temas relacionados](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Compatibilidad con valores altos de PPP en Direct2D

Direct2D proporciona las siguientes características para trabajar con escenarios de valores altos de PPP:

-   Respeta automáticamente el PPP del sistema al crear un destino de representación en ventanas, siempre que el manifiesto de aplicación indique que la aplicación controla ppp correctamente. (Para obtener información sobre cómo declarar que la aplicación tiene reconocimiento de PPP, vea [How to Ensure That Your Application Displays Properly on High-PPP Displays](how-to--size-a-window-properly-for-high-dpi-displays.md)[Cómo asegurarse de que la aplicación se muestra correctamente en pantallas con valores altos de PPP]).
-   Expresa coordenadas en DIP (píxeles independientes del dispositivo), lo que permite que la aplicación se escale automáticamente cuando cambia la configuración de PPP.
-   Permite que los mapas de bits tengan un VALOR DE PPP y los escala correctamente teniendo en cuenta el valor de PPP. Esta característica también se puede usar para mantener iconos en diferentes resoluciones.
-   Expresa la mayoría de los recursos en las DIP, lo que hace que los recursos sea automáticamente independiente de la resolución.
-   Usa un espacio de coordenadas de punto flotante y suavizado de contorno, por lo que cualquier contenido se puede escalar a cualquier PPP arbitrario.

La canalización de gráficos de Direct2D está diseñada para escalar de 96 PPP a 1200DPI.

## <a name="windows-8-and-high-dpi"></a>Windows 8 y valores altos de PPP

A partir Windows 8, hay características adicionales para la compatibilidad con valores altos de PPP.

Si el valor de PPP del contexto del dispositivo es lo suficientemente alto, Direct2D cambia el umbral que usa para habilitar el suavizado de contorno vertical del texto. Esto da como resultado una representación de texto más rápida en pantallas de valores altos de PPP. Además, puede cambiar el modo de unidad a píxeles en lugar de DIP mediante el [**método ID2D1DeviceContext::SetUnitMode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) Si establece el modo de unidad en píxeles y el valor de PPP del contexto del dispositivo en el VALOR DE PPP de la pantalla, la optimización todavía está habilitada.

## <a name="what-is-a-dip"></a>¿Qué es una DIP?

Un píxel independiente del dispositivo (DIP) es un píxel lógico que se asigna a los píxeles del dispositivo físico a través de un valor escalar, el ppp. PPP significa puntos por pulgada, donde un punto representa un píxel de dispositivo físico. (La nomenclatura procede de la impresión, donde los puntos son el punto de entrada de lápiz más pequeño que puede producir un proceso de impresión). Dado que un monitor estándar solía tener 96 puntos por pulgada, un ppp de 96 significaba que un píxel independiente del dispositivo (o DIP) asignaba 1:1 con un píxel físico. Por ejemplo, si el valor de PPP fuera 96 \* 2 = 192, una sola DIP abarcaría dos píxeles físicos.

Hay muchas razones por las que las aplicaciones no controlan necesariamente este escalado correctamente. Una de las razones más sencillas es que requiere trabajo adicional para detectar y usar este valor escalar al representar. En Direct2D, el escalado se aplica de forma predeterminada. Debido a esta asignación, los píxeles de dispositivo físico pueden acabar en coordenadas DIP fraccionales, que es uno de los motivos por los que Direct2D usa un espacio de coordenadas de punto flotante.

<dl> píxel físico = (dip × PPP) / 96  
</dl>

Para convertir un píxel físico en una DIP, use esta fórmula:

<dl> dip = (píxel físico × 96) / PPP  
</dl>

> [!Note]
>
> A partir Windows 8, puede cambiar el modo de unidad a píxeles en lugar de DIP mediante el [**método ID2D1DeviceContext::SetUnitMode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo asegurarse de que la aplicación se muestra correctamente en pantallas con valores altos de PPP](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 