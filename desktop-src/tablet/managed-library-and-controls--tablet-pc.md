---
description: Para compilar aplicaciones de Tablet PC en C \# y Visual Basic .net, el proyecto en Microsoft Visual Studio .net debe incluir una referencia a los ensamblados de biblioteca administrada de Tablet PC. Esto proporciona acceso al modelo de objetos administrados y a los controles.
ms.assetid: d9c491c9-d341-4189-9a41-45c4d78322fa
title: Biblioteca administrada y controles (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7299a1df0cc1b64d650ec748eb2de01ad4b776f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716716"
---
# <a name="managed-library-and-controls-tablet-pc"></a>Biblioteca administrada y controles (Tablet PC)

Para compilar aplicaciones de Tablet PC en C \# y Visual Basic .net, el proyecto en Microsoft Visual Studio .net debe incluir una referencia a los ensamblados de biblioteca administrada de Tablet PC. Esto proporciona acceso al modelo de objetos administrados y a los controles.

## <a name="microsoft-visual-c-and-visual-basicnet"></a>Microsoft Visual C \# y visual Basic.net

En Windows Vista, los ensamblados de biblioteca administrada de Tablet PC se instalan de forma predeterminada en dos directorios:

-   <systemdrive>: Archivos de \\ programa archivos \\ comunes \\ Directorio de tinta compartida de Microsoft \\
-   <systemdrive>: \\ Archivos de programa \\ Microsoft SDK \\ Windows \\ v 6.0 \\ bin

Para agregar una referencia a las bibliotecas administradas de la plataforma de Tablet PC en Microsoft Visual Studio .NET:

1.  Abra el proyecto de Visual Studio .NET.
2.  En el menú **Proyecto**, haga clic en **Agregar referencia**.
3.  En la pestaña **.net** del cuadro de diálogo **Agregar referencia** , en la lista componentes, seleccione **Microsoft Tablet PC API**.
4.  Haga clic en **seleccionar** y, a continuación, en **Aceptar**.

Para agregar una referencia a las API de análisis de tinta en Visual Studio .NET:

1.  Abra el proyecto Microsoft Visual Studio .NET.
2.  En el menú **Proyecto**, haga clic en **Agregar referencia**.
3.  En la pestaña **.net** del cuadro de diálogo **Agregar referencia** , en la lista componentes, seleccione **biblioteca administrada del análisis de tinta de Microsoft Tablet PC**.
4.  Haga clic en **seleccionar** y, a continuación, en **Aceptar**.

> [!Note]  
> Al compilar aplicaciones que usan Microsoft. Ink en Visual Studio 2005, debe seleccionar **proyecto**, seleccionar **propiedades**, seleccionar **compilar** y establecer destino de plataforma = x86. Esta opción no está disponible en Microsoft Visual Studio Express productos.

 

 

 



