---
title: Portar defs, binds y sets
description: Portar defs, binds y sets
ms.assetid: 971feb14-ed39-4492-a62b-9930bdc506e9
keywords:
- Porte de IRIS GL, definiciones
- porte desde IRIS GL, definiciones
- porte a OpenGL desde IRIS GL, definiciones
- Porte de OpenGL desde IRIS GL, definiciones
- Porte de IRIS GL,binds
- portar desde IRIS GL,binds
- portar a OpenGL desde IRIS GL, enlaza
- Portar OpenGL desde IRIS GL, enlaza
- Porte de IRIS GL, conjuntos
- porting from IRIS GL,sets
- porte a OpenGL desde IRIS GL, conjuntos
- Porte de OpenGL desde IRIS GL, conjuntos
- definitions
- Ata
- conjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a4c3776d3e5eb8000a4e81578bb5df95658a37e0793944a9cda6923fc7a2e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132667"
---
# <a name="porting-defs-binds-and-sets"></a>Portar defs, binds y sets

OpenGL no tiene tablas de definiciones almacenadas; No se pueden definir modelos de iluminación, material, texturas, estilos de línea o patrones como objetos independientes como se puede en IRIS GL. Por lo tanto, OpenGL no tiene equivalentes directos a las siguientes funciones GL de IRIS:

-   **Imdef** e **Imbind**
-   **tevdef** y **tevbind**
-   **textdef** y **textbind**
-   **definestyle** y **setstyle**
-   **defpattern** y **setpattern**

Puede usar listas de visualización de OpenGL para imitar el mecanismo de def/bind de IRIS GL. Por ejemplo, esta es una definición de material en IRIS GL:


```C++
float mat() = { 
    AMBIENT, .1, .1, .1, 
    DIFFUSE, 0, .369, .165, 
    SPECULAR, .5, .5, .5, 
    SHININESS, 10, 
    LMNULL 
}; 
lmdef(DEFMATERIAL, 1, 0, mat); 
lmbind(MATERIAL, 1);
```



El siguiente ejemplo de código OpenGL define el mismo material en una lista de visualización a la que hace referencia el número de lista definido **por MYMATERIAL.**


```C++
#define MYMATERIAL 10 
 
GLfloat        mat_amb[] = {.1, .1, .1, 1.0}; 
GLfloat        mat_dif[] = {0, .369, .165, 1.0}; 
GLfloat        mat_spec[] = {.5, .5, .5, 1.0}; 
 
glNewList(MYMATERIAL, GL_COMPILE); 
    glMaterialfv(GL_FRONT, GL_AMBIENT, mat_amb); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_dif); 
    glMaterialfv(GL_FRONT, GL_SHININESS, 10); 
glEndList(); 
 
glCallList( MYMATERIAL );
```



 

 




