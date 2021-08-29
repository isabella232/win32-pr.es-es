---
title: DirectWrite (DWrite)
description: Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad completa con texto Unicode y diseño. DirectWrite, una API [de DirectX,](../directx.md) proporciona estas características y mucho más.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca8efbc3c4824019d9a61e24a25a3ad5bb69f0e2c810250f11bfdb706c2fc96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071729"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Propósito

Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad completa con texto Unicode y diseño. DirectWrite, una API [de DirectX,](../directx.md) proporciona estas características y mucho más.

- Un sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.
- Representación de texto de [Microsoft ClearType](/typography/cleartype/) de alta calidad, subpíxel que puede usar [GDI,](interoperating-with-gdi.md) [Direct2D](rendering-by-using-direct2d.md)o tecnología de representación específica de la aplicación.
- Texto acelerado por hardware, cuando se usa [con Direct2D.](rendering-by-using-direct2d.md)
- Compatibilidad con texto de formato múltiple.
- Compatibilidad con las características avanzadas de tipografía de las fuentes OpenType.
- Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos.
- Diseño y representación compatibles con [GDI.](interoperating-with-gdi.md)

La API admite la medición, el dibujo y las pruebas de acceso de texto de varios formatos. DirectWrite texto en todos los idiomas admitidos para aplicaciones globales y localizadas, a partir de la infraestructura de lenguaje clave que se encuentra en Windows 7. DirectWrite también ofrece una API de representación de glifos de bajo nivel para los desarrolladores que quieren realizar su propio diseño y procesamiento de Unicode a glifo.

> [!NOTE]
> [Windows App SDK](/windows/apps/windows-app-sdk/) presenta una nueva versión de DirectWrite denominada DWriteCore que se ejecuta en versiones de Windows hasta Windows 8 y abre la puerta para que la use entre &mdash; plataformas. &mdash; Para obtener más información, vea [Introducción a DWriteCore.](dwritecore-overview.md)

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

- Windows 7 o Windows Vista con Service Pack 2 (SP2) y Platform Update para Windows Vista
- Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y actualización de plataforma para Windows Server 2008

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Novedades de DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Estas son algunas de las nuevas adiciones a DirectWrite. <br/> |
| [Guía de programación](programming-guide.md)<br/> | En los temas siguientes se proporciona información general sobre DirectWrite API.<br/> |
| [Referencia de API](reference.md)<br/> | Describe el DirectWrite API.<br/> |
| [Código de ejemplo](samples.md)<br/> | Esta sección contiene información sobre programas de ejemplo para DirectWrite.<br/> |
