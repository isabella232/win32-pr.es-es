---
description: Para compilar aplicaciones de Tablet PC en C y Visual Basic .NET, el proyecto de Microsoft Visual Studio .NET debe incluir una referencia a los ensamblados de biblioteca administrada de \# Tablet PC. Esto proporciona acceso al modelo de objetos administrados y a los controles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Biblioteca y controles administrados (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b4096ba54d3cd882b3ee50469d94792b4a46ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574469"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Biblioteca y controles administrados (Tablet PC)

Para compilar aplicaciones de Tablet PC en C y Visual Basic .NET, el proyecto de Microsoft Visual Studio .NET debe incluir una referencia a los ensamblados de biblioteca administrada de \# Tablet PC. Esto proporciona acceso al modelo de objetos administrados y a los controles.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# y Visual Basic.NET

En Windows Vista, los ensamblados de biblioteca administrada de Tablet PC se instalan de forma predeterminada en dos directorios:

-   &lt;&gt;systemdrive: Archivos de programa Common Files Directorio de Microsoft Shared \\ \\ \\ \\ Ink
-   &lt;&gt;systemdrive: archivos de programa sdk de Microsoft Windows bin \\ \\ \\ \\ v6.0 \\

Para agregar una referencia a las bibliotecas administradas de la plataforma tablet PC Microsoft Visual Studio .NET:

1.  Abra el Visual Studio proyecto de .NET.
2.  En el menú **Proyecto**, haga clic en **Agregar referencia**.
3.  En la **pestaña .NET del** cuadro de **diálogo** Agregar referencia, en la lista de componentes, seleccione Microsoft Tablet **PC API.**
4.  Haga clic **en Seleccionar** y, a continuación, **en Aceptar.**

Para agregar una referencia a las API de análisis de entrada de lápiz Visual Studio .NET:

1.  Abra el Microsoft Visual Studio proyecto de .NET.
2.  En el menú **Proyecto**, haga clic en **Agregar referencia**.
3.  En la **pestaña .NET del** **cuadro** de diálogo Agregar referencia , en la lista de componentes, seleccione Microsoft Tablet PC Ink Analysis **Managed Library**.
4.  Haga clic **en Seleccionar** y, a continuación, **en Aceptar.**

> [!Note]  
> Al compilar aplicaciones que usan Microsoft.Ink en Visual Studio 2005, debe seleccionar **Project**,  seleccionar **Propiedades,** seleccionar Compilar y establecer Destino de plataforma=x86. Esta opción no está disponible en Microsoft Visual Studio Express productos.

 

 

 



