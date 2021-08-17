---
description: En este tema se presenta cómo imprimir desde un programa Windows nativo mediante GDI&\# 160; Imprimir&\# 160; Api.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Cómo: Imprimir mediante la API de impresión de GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19832ef93a80cc537d16136ac751cb20fd8664d7d1d31d295568de68d6dd846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091935"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>Cómo: Imprimir mediante la API de impresión de GDI

En este tema se presenta cómo imprimir desde un programa Windows nativo mediante [la API de impresión de GDI](gdi-printing.md).

## <a name="overview"></a>Información general

La impresión suele ser una parte integral de un programa Windows nativo, por lo que no es una característica que se pueda agregar fácilmente después de haber escrito el programa. Al diseñar un programa para Windows 7, debe considerar el uso de [XPS Print API](xps-printing.md) para proporcionar la funcionalidad de impresión, ya que proporciona la mayor compatibilidad para el futuro. Los programas que deben ejecutarse en Windows Vista y versiones anteriores de Windows probablemente usarán la API de [impresión de GDI](gdi-printing.md) para proporcionar funcionalidad de impresión. La API de impresión de GDI también se admite en Windows 7, pero es más limitada que xpS Print API.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de la impresión](using-printing.md)
</dt> <dt>

[Cómo imprimir desde una aplicación Windows aplicación](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



