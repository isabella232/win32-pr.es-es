---
description: En esta sección se describe cómo configurar el entorno para usar las bibliotecas COM de la plataforma tablet PC en C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Biblioteca COM y ActiveX controles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bc76f9caa2bcb72fe26ed2e01e251c977f87ce01c12794aad78608d2f5887f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009095"
---
# <a name="com-library-and-activex-controls"></a>Biblioteca COM y ActiveX controles

En esta sección se describe cómo configurar el entorno para usar las bibliotecas COM de la plataforma tablet PC en C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Para compilar aplicaciones de Tablet PC en Visual C++, debe actualizar las variables de entorno del sistema, configurar las opciones de directorio para Visual Studio y acceder a las interfaces de Tablet PC en el proyecto.

Para actualizar las variables de entorno, siga las instrucciones proporcionadas por el SDK de Windows para agregar las variables de entorno a Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Acceso a las interfaces de Tablet PC

Para acceder a las interfaces de Tablet PC, debe incluir los archivos Ms ashut.h y Msgniut \_ i.c en el proyecto.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



También puede usar la siguiente directiva de importación en lugar de las instrucciones \# include enumeradas anteriormente.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Para acceder a las interfaces InkAnalysis, debe incluir los archivos IACom.h e IACom \_ i.c en el proyecto.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



También puede usar la siguiente directiva de importación en lugar de las instrucciones \# include enumeradas anteriormente.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Para acceder a las interfaces [**InkDivider,**](inkdivider-class.md) debe incluir los archivos msdivut15 \_ i.c y msdivut15.h en el proyecto.

> [!Note]  
> InkDivider se ha reemplazado por las API de análisis de lápiz.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



También puede usar la siguiente directiva de importación en lugar de las \# instrucciones include.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Para acceder a las interfaces [**PenInputPanel,**](peninputpanel-class.md) debe incluir los archivos PenInputPanel \_ i.c y PenInputPanel.h en el proyecto.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



También puede usar la siguiente directiva de importación en lugar de las \# instrucciones include.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> Las nuevas interfaces del panel de entrada de texto han reemplazado las API penInputPanel en Windows Vista.

 

Para acceder a las interfaces [InkEdit](inkedit-control-reference.md) Control, debe incluir los archivos Inked.h e Inked \_ i.c en el proyecto.


```C++
#include <inked.h>
#include <inked_i.c>
```



Como alternativa, puede \# importar el archivo InkEd.dll archivo.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



