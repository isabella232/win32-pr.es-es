---
description: Para compilar aplicaciones de Tablet PC en C y Visual Basic .NET, el proyecto de Microsoft Visual Studio .NET debe incluir una referencia a los ensamblados de biblioteca administrada de \# Tablet PC. Esto proporciona acceso al modelo de objetos administrados y a los controles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Biblioteca y controles administrados (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d031a97226d200b99a6d36b42e3e4c43862f5b6ac52203ee4ca08d1e5714f2c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119031733"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Biblioteca y controles administrados (Tablet PC)

Para compilar aplicaciones de Tablet PC en C y Visual Basic .NET, el proyecto de Microsoft Visual Studio .NET debe incluir una referencia a los ensamblados de biblioteca administrada de \# Tablet PC. Esto proporciona acceso al modelo de objetos administrados y a los controles.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# y Visual Basic.NET

En Windows Vista, los ensamblados de biblioteca administrada de Tablet PC se instalan de forma predeterminada en dos directorios:

-   <systemdrive>: archivos \\ de programa common files directorio de Microsoft Shared \\ \\ \\ Ink
-   <systemdrive>: \\ archivos de programa sdk de Microsoft Windows bin \\ \\ \\ v6.0 \\

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
> Al compilar aplicaciones que usan Microsoft.Ink en Visual Studio 2005, debe seleccionar **Project**, seleccione **Propiedades,** seleccione **Compilar** y establezca Platform target=x86. Esta opción no está disponible en Microsoft Visual Studio Express productos.

 

 

 



