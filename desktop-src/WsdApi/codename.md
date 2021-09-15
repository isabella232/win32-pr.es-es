---
description: Define el nombre que se va a usar para identificar el espacio de nombres en el código generado.
ms.assetid: 4e476be2-fa73-4b3e-b0cc-799c8d16b5de
title: elemento codeName
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9be7292135e79477d0a66d2a0667ebd51bd7567c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359387"
---
# <a name="codename-element"></a>elemento codeName

Define el nombre que se va a usar para identificar el espacio de nombres en el código generado.

## <a name="usage"></a>Uso

``` syntax
<codeName/>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios

No hay elementos secundarios.

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                         | Descripción                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|
| [**Nombres**](namespace.md)<br/>                       | Espacio de nombres que se usará para la generación de código.<br/> <br/>       |
| [**portTypeDeclarations**](porttypedeclarations.md)<br/> | Genera declaraciones constantes de C para tipos de puerto.<br/> <br/> |
| [**portTypeDefinitions**](porttypedefinitions.md)<br/>   | Genera constantes de C para tipos de puerto.<br/> <br/>             |



## <a name="remarks"></a>Observaciones

Este elemento invalida el nombre de código predeterminado utilizado para el código generado. De forma predeterminada, el código generado crea un nombre de código a partir del URI o nombre completo.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | Sí           |



 

 




