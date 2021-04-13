---
title: Herencia de tipos de Pointer-Attribute
description: Según la especificación de DCE, cada archivo IDL debe definir atributos para sus punteros.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421230"
---
# <a name="pointer-attribute-type-inheritance"></a>Herencia de tipos de Pointer-Attribute

Según la especificación de DCE, cada archivo IDL debe definir atributos para sus punteros. Si no se asigna un atributo explícito a un puntero, el puntero utiliza el valor especificado por la \[ palabra clave [ \_ default del puntero](/windows/desktop/Midl/pointer-default) \] . Algunas implementaciones de DCE no permiten punteros sin atributos. Si un puntero no tiene un atributo explícito, el archivo IDL debe tener una especificación **\[ \_ predeterminada \] de puntero** para que se pueda establecer el atributo de puntero.

En el modo predeterminado (extensiones de Microsoft), puede especificar el atributo de un puntero en el archivo IDL que importa el archivo de definición de IDL. Los punteros definidos en un archivo IDL pueden heredar atributos que se especifican en otros archivos IDL. Además, en el modo predeterminado, los archivos IDL pueden incluir punteros sin atributos. Si ni la base ni los archivos IDL importados especifican un atributo de puntero o el **\[ \_ valor predeterminado \] de puntero**, los punteros sin atributos se interpretan como punteros únicos.

El compilador MIDL asigna atributos de puntero a punteros utilizando las siguientes reglas de prioridad (1 es la más alta).



| Prioridad | Descripción                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Los atributos de puntero explícitos se aplican al puntero en la definición o el sitio de uso.                                      |
| 2        | El valor predeterminado es el atributo **\[ \_ predeterminado \] del puntero** en el archivo IDL que define el tipo.                               |
| 3        | El valor predeterminado es el atributo **\[ \_ predeterminado \] del puntero** en el archivo IDL que importa el tipo.                               |
| 4        | El valor predeterminado es \[ [ptr](/windows/desktop/Midl/ptr) \] en modo de compatibilidad de DCE o \[ [único](/windows/desktop/Midl/unique) \] en el modo de extensiones de Microsoft. |



 

 

 