---
description: En esta sección se describe cómo configurar el entorno para usar las bibliotecas COM de la plataforma de Tablet PC en C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Biblioteca COM y controles ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705442"
---
# <a name="com-library-and-activex-controls"></a>Biblioteca COM y controles ActiveX

En esta sección se describe cómo configurar el entorno para usar las bibliotecas COM de la plataforma de Tablet PC en C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Para compilar aplicaciones de Tablet PC en Visual C++, debe actualizar las variables de entorno del sistema, configurar las opciones de directorio de Visual Studio y tener acceso a las interfaces de Tablet PC en el proyecto.

Para actualizar las variables de entorno, siga las instrucciones proporcionadas por el Windows SDK para agregar las variables de entorno a Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Acceso a las interfaces de Tablet PC

Para tener acceso a las interfaces de Tablet PC, debe incluir los archivos Msinkaut. h y Msinkaut \_ i. c en el proyecto.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include enumeradas anteriormente.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Para tener acceso a las interfaces de InkAnalysis, debe incluir los archivos IACom. h y IACom \_ i. c en el proyecto.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include enumeradas anteriormente.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Para tener acceso a las interfaces de [**InkDivider**](inkdivider-class.md) , debe incluir \_ los archivos msinkaut15 i. c y msinkaut15. h en el proyecto.

> [!Note]  
> InkDivider ha sido sustituido por las API de análisis de tinta.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Para tener acceso a las interfaces de [**PenInputPanel**](peninputpanel-class.md) , debe incluir \_ los archivos PenInputPanel i. c y PenInputPanel. h en el proyecto.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



También puede utilizar la siguiente directiva de importación en lugar de las \# instrucciones include.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> Las API de PenInputPanel se han sustituido en Windows Vista por las nuevas interfaces del panel de entrada de texto.

 

Para tener acceso a las interfaces de control de [InkEdit](inkedit-control-reference.md) , debe incluir los archivos. h y. \_ c interactivos en el proyecto.


```C++
#include <inked.h>
#include <inked_i.c>
```



Como alternativa, puede \# importar el archivo de InkEd.dll.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



