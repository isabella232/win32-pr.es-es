---
title: Enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI
description: Una interfaz dual permite el acceso de vtable directo a todas sus funciones mientras no una interfaz de envío.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI ADSI
- extensiones ADSI, enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI
- ADSI ADSI, Visual Basic de código de ejemplo, uso de IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656414"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Enlace en tiempo de ejecución frente al acceso a vtable en el modelo de extensión ADSI

Una interfaz dual permite el acceso de vtable directo a todas sus funciones mientras no una interfaz de envío. Un cliente de C/C++ puede consultar un puntero de interfaz dual y usar el acceso de vtable directo para invocar sus funciones. Esto proporciona un acceso más rápido que la invocación de la función mediante las funciones [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) y [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) . Esto es especialmente cierto en el modelo de extensión, ya que todas las interfaces duales de un objeto de extensión deben delegar sus funciones **GetIDsOfNames** e **Invoke** primero al agregador (ADSI). Después, el agregador debe realizar pasos internos adicionales para identificar qué objeto de extensión, posiblemente incluido el propio agregador, proporciona compatibilidad para la función llamada y redirige la llamada al objeto adecuado.

Visual Basic también invoca una función de interfaz dual mediante el acceso directo a una tabla vtable, si tiene un puntero a la interfaz y acceso a los datos de tipo de la biblioteca de tipos. Los clientes ADSI escritos en Visual Basic pueden especificar un puntero a una interfaz dual, como [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explícitamente, y, por tanto, habilitar el acceso de vtable a las funciones de la interfaz.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Dado que una interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) no admite el acceso a vtable, no se aplica este ejemplo. Es decir, siempre se invoca una función de envío a través de las funciones [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) y [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) únicamente.

Las versiones actuales de VBScript y JScript tampoco admiten el acceso vtable. Por lo tanto, una interfaz dual en un entorno de VBScript o JScript funciona como una interfaz de envío.

 

 