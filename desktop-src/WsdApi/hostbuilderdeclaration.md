---
description: Genera una declaración para una función que crea un host con tipo.
ms.assetid: 3c08e913-b47e-4ca7-b8bc-7b036e57db01
title: elemento hostBuilderDeclaration
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf3ddd474b4000b053b49157f1fc4b2eb399d34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070360"
---
# <a name="hostbuilderdeclaration-element"></a>elemento hostBuilderDeclaration

Genera una declaración para una función que crea un host con tipo.

## <a name="usage"></a>Uso

``` syntax
<hostBuilderDeclaration>
  child elements
</hostBuilderDeclaration>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                                   | Descripción                                                                                                                                                                                                                  |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**interfaz**](interface.md)<br/> | Nombre de la interfaz de servicio que se va a incluir para el host. El valor de este elemento debe coincidir con el valor del elemento secundario [**de**](interface.md) interfaz [**de hostedService**](hostedservice.md). <br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
interface+
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                         | Descripción                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Archivo**](file.md)<br/> | Genera un archivo del generador de código.<br/> <br/> |



## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




