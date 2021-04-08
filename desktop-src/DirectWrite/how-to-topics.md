---
title: Temas de procedimientos (DirectWrite)
description: En los temas siguientes se proporciona información general sobre la API de DirectWrite.
ms.assetid: da4817ee-0bff-433f-b595-4250199bcc14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a26bbb4500ab016fbf5a5a59f6b551030e28dd1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078748"
---
# <a name="how-to-topics-directwrite"></a>Temas de procedimientos (DirectWrite)

En los temas siguientes se proporciona información general sobre la API de [DirectWrite](direct-write-portal.md) .

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cómo alinear texto](how-to-align-text.md)<br/>                                                                                                                   | Puede alinear el texto de [DirectWrite](direct-write-portal.md) mediante el método [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) de la interfaz [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)<br/>                                                                                                                                                                                                               |
| [Cómo agregar compatibilidad para varios monitores](how-to-add-support-for-multiple-monitors.md)<br/>                                                                     | [DirectWrite](direct-write-portal.md) incluye compatibilidad con sistemas con varios monitores. Los distintos monitores pueden tener diferentes geometrías de píxeles (RGB, BGR o FLAT) u otros atributos. Para obtener más información acerca de la geometría de píxeles, vea el tema de referencia de la [**\_ \_ geometría de DWRITE píxeles**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry) . En este tema se muestra cómo agregar compatibilidad para varios monitores a la aplicación de DirectWrite. <br/> |
| [Cómo asegurarse de que la aplicación se muestre correctamente en pantallas de alta resolución de PPP](how-to-ensure-that-your-application-displays-properly-on-high-dpi-displays.md)<br/> | Describe cómo crear una ventana que se muestra correctamente en pantallas de alta ppp.<br/>                                                                                                                                                                                                                                                                                                                                               |
| [Cómo asegurarse de que el texto se muestra con la dirección de lectura correcta](how-to-ensure-text-is-displayed-with-the-correct-reading-direction.md)<br/>                 | Algunos idiomas, como el árabe y el hebreo, requieren una dirección de lectura de derecha a izquierda. Para un objeto de formato de texto [DirectWrite](direct-write-portal.md) , la dirección de lectura predeterminada es de izquierda a derecha. DirectWrite no infiere automáticamente la dirección de lectura de la configuración regional, por lo que debe hacerlo usted mismo.<br/>                                                                                                   |
| [Cómo enumerar fuentes](font-enumeration.md)<br/>                                                                                                               | En esta información general se muestra cómo enumerar las fuentes de la colección de fuentes del sistema, por nombre de familia.<br/>                                                                                                                                                                                                                                                                                                                          |
| [Cómo realizar pruebas de posicionamiento en un diseño de texto](how-to-perform-hit-testing-on-a-text-layout.md)<br/>                                                               | Proporciona un breve tutorial sobre cómo agregar pruebas de posicionamiento a una aplicación de [DirectWrite](direct-write-portal.md) que muestre texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                  |
| [Cómo agregar objetos alineados a un diseño de texto](how-to-add-inline-objects-to-a-text-layout.md)<br/>                                                                 | Proporciona un breve tutorial sobre cómo agregar objetos insertados a una aplicación de [DirectWrite](direct-write-portal.md) que muestra texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . <br/>                                                                                                                                                                                                                         |
| [Cómo agregar efectos de dibujo de cliente a un diseño de texto](how-to-add-custom-drawing-efffects-to-a-text-layout.md)<br/>                                                | Proporciona un breve tutorial sobre cómo agregar efectos de dibujo de cliente a una aplicación de [DirectWrite](direct-write-portal.md) que muestra texto mediante la interfaz [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) y un representador de texto personalizado. <br/>                                                                                                                                                                                      |



 

 

