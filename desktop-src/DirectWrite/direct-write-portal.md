---
title: DirectWrite (DWrite)
description: Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad con el diseño y el texto Unicode completo. DirectWrite, una API de [DirectX](../directx.md) , proporciona estas características y mucho más.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b1e2ff44083a56a7202847fc07ad9daaa67b7ba
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2020
ms.locfileid: "104488908"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Propósito

Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad con el diseño y el texto Unicode completo. DirectWrite, una API de [DirectX](../directx.md) , proporciona estas características y mucho más.

- Sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.
- Representación de texto de alta calidad, subpíxel, [ClearType de Microsoft](/typography/cleartype/) que puede usar la tecnología de representación de [GDI](interoperating-with-gdi.md), [Direct2D](rendering-by-using-direct2d.md)o específica de la aplicación.
- Texto con aceleración de hardware, cuando se usa con [Direct2D](rendering-by-using-direct2d.md).
- Compatibilidad con texto con varios formatos.
- Compatibilidad con las características tipográficas avanzadas de las fuentes OpenType.
- Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos.
- Diseño y representación compatibles con [GDI](interoperating-with-gdi.md).

La API admite la medición, el dibujo y la prueba de posicionamiento de texto multiformato. DirectWrite controla el texto en todos los idiomas admitidos para las aplicaciones globales y localizadas, y se basa en la infraestructura de idioma clave que se encuentra en Windows 7. DirectWrite también ofrece una API de representación de glifos de bajo nivel para los desarrolladores que quieren realizar su propio diseño y procesamiento de Unicode a glifo.

> [!NOTE]
> [Project reunion](/windows/apps/project-reunion/) presenta una nueva versión de DirectWrite &mdash; llamada DWriteCore &mdash; que se ejecuta en versiones de Windows hasta Windows 8 y abre la puerta para que la use entre plataformas. Para obtener más información, consulte [información general de DWriteCore](dwritecore-overview.md).

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

- Windows 7 o Windows Vista con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Vista
- Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y la actualización de la plataforma para Windows Server 2008

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Novedades de DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Estas son algunas de las nuevas adiciones a DirectWrite. <br/> |
| [Guía de programación](programming-guide.md)<br/> | En los temas siguientes se proporciona información general sobre la API de DirectWrite.<br/> |
| [Referencia de API](reference.md)<br/> | Describe la API de DirectWrite.<br/> |
| [Código de ejemplo](samples.md)<br/> | Esta sección contiene información sobre los programas de ejemplo de DirectWrite.<br/> |
