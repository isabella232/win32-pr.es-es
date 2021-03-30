---
title: Búfer de Application-Allocated
description: El atributo ACF \ byte \_ Count \ indica al código auxiliar que use un búfer preasignado que no se haya asignado ni liberado por las rutinas de soporte técnico del cliente.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db533495f16d37aca0bdae96035783650573a60f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488119"
---
# <a name="application-allocated-buffer"></a>Búfer de Application-Allocated

El \[ [**\_ número de bytes**](/windows/desktop/Midl/byte-count) del atributo ACF \] indica al código auxiliar que utilice un búfer preasignado que no están asignados ni liberado por las rutinas de soporte técnico del cliente. El \[ atributo de **\_ recuento de bytes** \] se aplica a un puntero o a un parámetro de matriz que apunta al búfer. Requiere un parámetro que especifique el tamaño del búfer en bytes.

El área de memoria asignada por el cliente puede contener estructuras de datos complejas con varios punteros. Dado que el área de memoria es contiguo, la aplicación no tiene que realizar varias llamadas para liberar cada puntero y estructura de forma individual. Al igual que cuando se usa el \[ atributo [**asignar (todos los \_ nodos)**](/windows/desktop/Midl/allocate) \] , el área de memoria se puede asignar o liberar con una llamada a la rutina de asignación de memoria o la rutina gratuita. Sin embargo, a diferencia de lo que ocurre con el atributo de \[ **asignación (todos los \_ nodos)** \] , el código auxiliar del cliente no administra el parámetro de búfer, sino que la aplicación cliente.

El búfer debe ser un \[ [](/windows/desktop/Midl/out-idl) \] parámetro de solo salida y la longitud del búfer en bytes debe ser un \[ [](/windows/desktop/Midl/in) \] parámetro solo en. El \[ [**atributo \_ recuento de bytes**](/windows/desktop/Midl/byte-count) \] solo se puede aplicar a tipos de puntero. El \[ atributo ACF de **\_ recuento de bytes** \] es una extensión de Microsoft a DCE IDL y, como tal, no está disponible si se compila con el modificador [**/OSF**](/windows/desktop/Midl/-osf) de MIDL.

En el ejemplo siguiente, el parámetro *pRoot* utiliza el recuento de bytes:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

El \[ [**atributo \_ recuento de bytes**](/windows/desktop/Midl/byte-count) \] aparece en el ACF como:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

El código auxiliar de cliente generado a partir de estos archivos IDL y ACF no asigna ni libera memoria para este búfer. El código auxiliar del servidor asigna y libera el búfer en una sola llamada utilizando el parámetro de tamaño proporcionado. Si los datos son demasiado grandes para el tamaño de búfer especificado, se produce una excepción.

 

 