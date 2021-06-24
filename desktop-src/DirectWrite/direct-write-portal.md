---
title: DirectWrite (DWrite)
description: Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad completa con texto Unicode y diseño. DirectWrite, una API [de DirectX,](../directx.md) proporciona estas características y mucho más.
ms.assetid: 62a8d723-ae1c-4cbc-a9da-3177e80d4a3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6bdc75845c2387a4fa4335fa462d0b97ec5669
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587952"
---
# <a name="directwrite-dwrite"></a>DirectWrite (DWrite)

## <a name="purpose"></a>Propósito

Las aplicaciones actuales deben admitir la representación de texto de alta calidad, las fuentes de esquema independientes de la resolución y la compatibilidad completa con texto Unicode y diseño. DirectWrite, una API [de DirectX,](../directx.md) proporciona estas características y mucho más.

- Un sistema de diseño de texto independiente del dispositivo que mejora la legibilidad del texto en documentos y en la interfaz de usuario.
- Representación de texto [ClearType](/typography/cleartype/) de Microsoft de alta calidad, sub píxeles que puede usar [GDI,](interoperating-with-gdi.md) [Direct2D](rendering-by-using-direct2d.md)o tecnología de representación específica de la aplicación.
- Texto acelerado por hardware, cuando se usa [con Direct2D.](rendering-by-using-direct2d.md)
- Compatibilidad con texto con varios formatos.
- Compatibilidad con las características de tipografía avanzadas de las fuentes OpenType.
- Compatibilidad con el diseño y la representación de texto en todos los idiomas admitidos.
- Diseño y representación compatibles con [GDI.](interoperating-with-gdi.md)

La API admite la medición, el dibujo y las pruebas de acceso del texto de varios formatos. DirectWrite controla el texto en todos los idiomas admitidos para aplicaciones globales y localizadas, a partir de la infraestructura de lenguaje clave que se encuentra en Windows 7. DirectWrite también ofrece una API de representación de glifos de bajo nivel para los desarrolladores que quieren realizar su propio diseño y procesamiento de Unicode a glifo.

> [!NOTE]
> [El SDK](/windows/apps/windows-app-sdk/) para aplicaciones de Windows presenta una nueva versión de DirectWrite denominada DWriteCore que se ejecuta en versiones de Windows hasta Windows 8 y abre la puerta para que la use &mdash; entre plataformas. &mdash; Para obtener más información, vea [Introducción a DWriteCore.](dwritecore-overview.md)

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

- Windows 7 o Windows Vista con Service Pack 2 (SP2) y actualización de plataforma para Windows Vista
- Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) y Platform Update para Windows Server 2008

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Novedades de DirectWrite](what-s-new-in-directwrite-for-windows-8-consumer-preview.md)<br/> | Estas son algunas de las nuevas adiciones a DirectWrite. <br/> |
| [Guía de programación](programming-guide.md)<br/> | En los temas siguientes se proporciona información general sobre DirectWrite API.<br/> |
| [Referencia de API](reference.md)<br/> | Describe directWrite API.<br/> |
| [Código de ejemplo](samples.md)<br/> | Esta sección contiene información sobre programas de ejemplo para DirectWrite.<br/> |
