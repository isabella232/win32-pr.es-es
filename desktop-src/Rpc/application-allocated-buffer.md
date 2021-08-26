---
title: Application-Allocated buffer
description: El atributo ACF \byte count\ dirige a los códigos auxiliares para que usen un búfer asignado previamente que las rutinas de soporte técnico del cliente no asignan ni \_ liberan.
ms.assetid: 1b370f74-394e-4e57-9749-83334be50f28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb87390637cba57cbdf4021a43f4ec98ea64c3828c67dfdb615ffcd62dc8c16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024185"
---
# <a name="application-allocated-buffer"></a>Application-Allocated buffer

El recuento de bytes del atributo ACF dirige a los códigos auxiliares para que usen un búfer asignado previamente que las rutinas de soporte técnico del cliente no asignan ni \[ [**\_**](/windows/desktop/Midl/byte-count) \] liberan. El \[ **atributo byte \_ count** \] se aplica a un puntero o parámetro de matriz que apunta al búfer. Requiere un parámetro que especifica el tamaño del búfer en bytes.

El área de memoria asignada por el cliente puede contener estructuras de datos complejas con varios punteros. Dado que el área de memoria es contigua, la aplicación no tiene que realizar varias llamadas para liberar cada puntero y estructura individualmente. Como cuando se usa el atributo \[ [**allocate(all \_ nodes),**](/windows/desktop/Midl/allocate) el área de memoria se puede asignar o liberar con una llamada a la rutina de asignación de memoria o a la \] rutina libre. Sin embargo, a diferencia del uso del atributo \[ **allocate(all \_ nodes),** el parámetro buffer no lo administra el código auxiliar del \] cliente, sino la aplicación cliente.

El búfer debe ser un parámetro de solo salida y la longitud del búfer \[ [](/windows/desktop/Midl/out-idl) \] en bytes debe ser \[ [**un parámetro solo**](/windows/desktop/Midl/in) \] en . El \[ [**atributo byte \_ count**](/windows/desktop/Midl/byte-count) \] solo se puede aplicar a tipos de puntero. El atributo ACF de recuento de bytes es una extensión de Microsoft para DCE IDL y, como tal, no está disponible si se compila mediante el modificador \[ **\_** \] MIDL [**/osf.**](/windows/desktop/Midl/-osf)

En el ejemplo siguiente, el parámetro *pRoot* usa el recuento de bytes:

``` syntax
/* function prototype in IDL file (fragment) */
void SortNames(
    [in] short cNames,
    [in, size_is(cNames)] STRINGTYPE pszArray[],
    [in] short cBytes,
    [out, ref] P_TREE_TYPE pRoot  /* tree with sorted data */
);
```

El \[ [**atributo byte \_ count**](/windows/desktop/Midl/byte-count) \] aparece en el ACF como:

``` syntax
/* ACF file (fragment) */
SortNames([byte_count(cBytes)] pRoot);
```

El código auxiliar de cliente generado a partir de estos archivos IDL y ACF no asigna ni libera la memoria para este búfer. El código auxiliar del servidor asigna y libera el búfer en una sola llamada mediante el parámetro de tamaño proporcionado. Si los datos son demasiado grandes para el tamaño de búfer especificado, se produce una excepción.

 

 