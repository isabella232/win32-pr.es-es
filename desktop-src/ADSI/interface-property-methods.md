---
title: Métodos de propiedad de interfaz
description: Muchas interfaces ADSI están diseñadas para admitir Automation y, por tanto, son interfaces duales, ya que admiten el acceso de cliente a través de las interfaces IUnknown e IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad de interfaz
- ADSI ADSI, referencia, métodos de propiedad explicados
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970419"
---
# <a name="interface-property-methods"></a>Métodos de propiedad de interfaz

Muchas interfaces ADSI están diseñadas para admitir Automation y, por tanto, son interfaces duales, ya que admiten el acceso de cliente a través de las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Los clientes que no son de Automation, como los escritos en C/C++, resuelven la invocación de métodos directamente mediante el método [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) y llaman al método directamente. Los clientes de Automation, también conocidos como clientes enlazados a nombres, como los escritos en Visual Basic o Visual Basic Scripting Edition (VBScript), deben resolver indirectamente la invocación de método mediante el método [**dispinterface.**](/previous-versions/windows/desktop/automat/dispinterface)

Una interfaz ADSI que admite Automation define métodos de propiedad para recuperar y modificar las propiedades de un objeto que implementa la interfaz. Los métodos de propiedad tienen nombres que tienen **get** y put anteponer a los nombres de propiedad adecuados, por \_  \_ ejemplo, **get \_ User** y **put \_ Name**.

Cada **\_ método get** toma un único parámetro como salida. Este parámetro es una dirección asignada por método de una variable del tipo de datos de propiedad . En la devolución, esta variable asume el valor actual de la propiedad solicitada. El autor de la llamada debe liberar la memoria asignada de la variable cuando la propiedad ya no sea necesaria.

Cada **\_ método put** toma un único parámetro como entrada para el tipo de datos de la propiedad correspondiente. El parámetro contiene un nuevo valor de la propiedad .

En el ejemplo de código siguiente se muestra la invocación de los métodos de propiedad que siguen el procedimiento habitual para llamar a la función miembro de un objeto .


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



En el ejemplo de código siguiente se muestra la invocación de los métodos de propiedad en clientes de automatización, que puede ser algo diferente. Por ejemplo, Visual Basic utiliza la notación de puntos.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



Todos los parámetros y tipos de valor devuelto deben ser de los que define el tipo de datos VARIANT. Todos los métodos de una interfaz dual devuelven un valor HRESULT para indicar que se ha hecho correctamente o no.

Para obtener más información sobre cómo obtener y establecer propiedades en objetos ADSI, vea [Caché de propiedades.](property-cache-interfaces.md)

 

 