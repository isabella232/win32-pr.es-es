---
description: En este tema se presenta cómo imprimir desde un programa de Windows nativo mediante el&GDI \# 160; Imprime&\# 160; API.
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 'Cómo: imprimir mediante la API de impresión de GDI'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913153"
---
# <a name="how-to-print-using-the-gdi-print-api"></a>Cómo: imprimir mediante la API de impresión de GDI

En este tema se explica cómo imprimir desde un programa nativo de Windows mediante la [API de impresión de GDI](gdi-printing.md).

## <a name="overview"></a>Información general

La impresión suele ser una parte integral de un programa de Windows nativo, por lo que no es una característica que se puede agregar fácilmente después de haber escrito el programa. Al diseñar un programa para Windows 7, debería considerar la posibilidad de usar la [API de impresión XPS](xps-printing.md) para proporcionar la funcionalidad de impresión porque proporciona la máxima compatibilidad para el futuro. Es más probable que los programas que se deben ejecutar en Windows Vista y versiones anteriores de Windows usen la [API de impresión GDI](gdi-printing.md) para proporcionar la funcionalidad de impresión. La API de impresión GDI también se admite en Windows 7, pero es más limitada que la API de impresión XPS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar la impresión](using-printing.md)
</dt> <dt>

[Cómo imprimir desde una aplicación de Windows](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



