---
description: Genera definiciones de estructura de C para tipos conocidos.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: Elemento structDefinitions
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996462"
---
# <a name="structdefinitions-element"></a>Elemento structDefinitions

Genera definiciones de estructura de C para tipos conocidos.

## <a name="usage"></a>Uso

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo del generador de código.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Gran parte del código generado y el código de aplicación hacen referencia a las estructuras para los tipos conocidos. Este elemento se usa para generar archivos de incluir. Este elemento debe producirse después de [**un elemento structDeclarations**](structdeclarations.md) para que las referencias entre estructuras se controlen correctamente.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




