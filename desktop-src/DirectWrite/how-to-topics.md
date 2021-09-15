---
title: Temas de ayuda (DirectWrite)
description: Vea los temas de cómo hacerlo en la guía de programación DirectWrite API. DirectWrite permite Windows aplicaciones para mejorar la experiencia de texto para la interfaz de usuario y los documentos.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc35d9b92001bc8c4807f8b77434559994aaac4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476953"
---
# <a name="how-to-topics-directwrite"></a>Temas de ayuda (DirectWrite)

En los temas siguientes se proporciona información general sobre [DirectWrite](direct-write-portal.md) API.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Alineación de texto](how-to-align-text.md)<br/>                                                                                                                   | Puede alinear [DirectWrite](direct-write-portal.md) texto mediante el [**método SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de la [**interfaz IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)<br/>                                                                                                                                                                                                               |
| [Cómo agregar compatibilidad con varios monitores](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) compatibilidad con sistemas con varios monitores. Los distintos monitores pueden tener diferentes geometrías de píxeles (RGB, BGR o FLAT) u otros atributos. Para obtener más información sobre la geometría de píxeles, vea el tema de referencia [**DWRITE \_ PIXEL \_ GEOMETRY.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) En este tema se muestra cómo agregar compatibilidad con varios monitores a la DirectWrite aplicación. <br/> |
| [Cómo asegurarse de que la aplicación se muestra correctamente en pantallas con valores altos de PPP](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Describe cómo crear una ventana que se muestra correctamente en pantallas con valores altos de PPP.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Cómo asegurarse de que el texto se muestra con la dirección de lectura correcta](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Algunos idiomas, como árabe y hebreo, requieren una dirección de lectura de derecha a izquierda. Para un objeto [DirectWrite](direct-write-portal.md) de texto, la dirección de lectura predeterminada es de izquierda a derecha. DirectWrite no deduce automáticamente la dirección de lectura de la configuración regional, por lo que debe hacerlo usted mismo.<br/>                                                                                                   |
| [Enumeración de fuentes](font-enumeration.md)<br/>                                                                                                               | En esta introducción se muestra cómo enumerar las fuentes de la colección de fuentes del sistema, por nombre de familia.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Cómo realizar pruebas de acceso en un diseño de texto](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Proporciona un breve tutorial sobre cómo agregar pruebas de acceso a una [aplicación DirectWrite](direct-write-portal.md) que muestra texto mediante la [**interfaz IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) <br/>                                                                                                                                                                                                                  |
| [Cómo agregar objetos en línea a un diseño de texto](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Proporciona un breve tutorial sobre cómo agregar objetos en línea a una [DirectWrite](direct-write-portal.md) que muestra texto mediante la [**interfaz IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) <br/>                                                                                                                                                                                                                         |
| [Cómo agregar efectos de dibujo de cliente a un diseño de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Proporciona un breve tutorial sobre cómo agregar efectos de dibujo de cliente a una aplicación [DirectWrite](direct-write-portal.md) que muestra texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) y un representador de texto personalizado. <br/>                                                                                                                                                                                      |



 

 

