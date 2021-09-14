---
title: Pointer-Attribute de tipos
description: Según la especificación de DCE, cada archivo IDL debe definir atributos para sus punteros.
ms.assetid: ab8821ce-d52a-42bf-aa5e-582bb24adf93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182b7d46774484a9520424fd82bcff2d7103aa3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161040"
---
# <a name="pointer-attribute-type-inheritance"></a>Pointer-Attribute de tipos

Según la especificación de DCE, cada archivo IDL debe definir atributos para sus punteros. Si no se asigna un atributo explícito a un puntero, el puntero usa el valor especificado por la palabra \[ [clave default \_ del](/windows/desktop/Midl/pointer-default) \] puntero. Algunas implementaciones de DCE no permiten punteros sin atributos. Si un puntero no tiene un atributo explícito, el archivo IDL **\[ \_ \]** debe tener una especificación predeterminada de puntero para poder establecer el atributo de puntero.

En el modo predeterminado (extensiones de Microsoft), puede especificar el atributo de un puntero en el archivo IDL que importa el archivo IDL de definición. Los punteros definidos en un archivo IDL pueden heredar atributos que se especifican en otros archivos IDL. Además, en el modo predeterminado, los archivos IDL pueden incluir punteros sin atributos. Si ni los archivos IDL **\[ \_ \]** base ni importados especifican un atributo de puntero o un puntero predeterminado, los punteros sin atributos se interpretan como punteros únicos.

El compilador MIDL asigna atributos de puntero a punteros mediante las siguientes reglas de prioridad (1 es la más alta).



| Prioridad | Descripción                                                                                                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|
| 1        | Los atributos de puntero explícitos se aplican al puntero en el sitio de definición o uso.                                      |
| 2        | El valor predeterminado es **\[ el atributo predeterminado \_ del \]** puntero en el archivo IDL que define el tipo.                               |
| 3        | El valor predeterminado es **\[ el atributo predeterminado \_ del \]** puntero en el archivo IDL que importa el tipo.                               |
| 4        | El valor predeterminado \[ [es ptr](/windows/desktop/Midl/ptr) en modo de compatibilidad con \] DCE o \[ [único en](/windows/desktop/Midl/unique) el modo \] de extensiones de Microsoft. |



 

 

 