---
title: Métodos de propiedad de interfaz
description: Muchas interfaces ADSI están diseñadas para admitir la automatización y, por tanto, son interfaces duales que admiten el acceso de cliente a través de interfaces IUnknown e IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad de interfaz
- ADSI ADSI, referencia y métodos de propiedad explicados
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656415"
---
# <a name="interface-property-methods"></a>Métodos de propiedad de interfaz

Muchas interfaces ADSI están diseñadas para admitir la automatización y, por tanto, son interfaces duales que admiten el acceso de cliente a través de interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Los clientes que no son de automatización, como los escritos en C/C++, resuelven la invocación de métodos directamente mediante el método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) y llaman al método directamente. Los clientes de automatización, también conocidos como clientes enlazados a nombres, como los escritos en Visual Basic o Visual Basic Scripting Edition (VBScript), deben resolver indirectamente la invocación de métodos mediante el método [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) .

Una interfaz ADSI que admite la automatización define métodos de propiedad para recuperar y modificar propiedades de un objeto que implementa la interfaz. Los métodos de propiedad tienen nombres que tienen **Get** \_ y **Put** \_ antepuesto a los nombres de propiedad adecuados, por ejemplo, **Get \_ User** y **Put \_ Name**.

Cada **método \_ Get** toma un parámetro único como output. Este parámetro es una dirección asignada por un método de una variable del tipo de datos de la propiedad. Al devolverse, esta variable asume el valor actual de la propiedad solicitada. El llamador debe liberar la memoria asignada de la variable cuando ya no se necesite la propiedad.

Cada **método \_ Put** toma un parámetro único como entrada para el tipo de datos de la propiedad correspondiente. El parámetro contiene un nuevo valor de la propiedad.

En el ejemplo de código siguiente se muestra la invocación de los métodos de propiedad que siguen el procedimiento habitual para llamar a la función miembro de un objeto.


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



En el ejemplo de código siguiente se muestra la invocación de los métodos de propiedad en los clientes de automatización, que puede ser algo diferente. Por ejemplo, Visual Basic usa la notación de puntos.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



Todos los parámetros y tipos devueltos deben ser de los que define el tipo de datos VARIANT. Todos los métodos de una interfaz dual devuelven un valor HRESULT para indicar si se ha realizado correctamente o no.

Para obtener más información sobre cómo obtener y establecer las propiedades de los objetos ADSI, vea [caché de propiedades](property-cache-interfaces.md).

 

 