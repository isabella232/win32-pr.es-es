---
title: Enlace en tiempo de tarde frente a acceso de Vtable en el modelo de extensión ADSI
description: Una interfaz dual permite el acceso directo de vtable a todas sus funciones, mientras que una interfaz de distribución no lo hace.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- enlace en tiempo de tarde frente a acceso vtable en adsi extension model ADSI
- extensiones ADSI, enlace en tiempo de tarde frente a acceso vtable en el modelo de extensión ADSI
- ADSI ADSI, código de ejemplo Visual Basic , mediante IADsDSDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eacc2008d3da33cd8d1897eeff2c30301849f9ec306656fc494072c33608c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023363"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Enlace en tiempo de tarde frente a acceso de Vtable en el modelo de extensión ADSI

Una interfaz dual permite el acceso directo de vtable a todas sus funciones, mientras que una interfaz de distribución no lo hace. Un cliente de C/C++ puede consultar un puntero de interfaz dual y usar el acceso directo a la tabla virtual para invocar sus funciones. Esto proporciona un acceso más rápido que invocar la función mediante las funciones [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) [**e IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) Esto es especialmente cierto en el modelo de extensión, porque todas las interfaces duales de un objeto de extensión deben delegar primero sus funciones **GetIDsOfNames** e **Invoke** en el agregador (ADSI). A continuación, el agregador debe realizar pasos internos adicionales para identificar qué objeto de extensión, posiblemente incluido el propio agregador, proporciona compatibilidad con la función llamada y redirigir la llamada al objeto adecuado.

Visual Basic invoca también una función de interfaz dual mediante el acceso directo a una tabla virtual, si tiene un puntero a la interfaz y acceso a los datos de tipo de la biblioteca de tipos. Los clientes ADSI escritos en Visual Basic pueden especificar un puntero a una interfaz dual, por ejemplo, los [**IAD**](/windows/desktop/api/Iads/nn-iads-iads), explícitamente y, por tanto, habilitar el acceso de vtable a las funciones de la interfaz.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Dado que [**una interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) no admite el acceso de vtable, este ejemplo no se aplica. Es decir, una función de distribución siempre se invoca a través de las funciones [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) únicamente.

Las versiones actuales de VBScript JScript tampoco admiten el acceso vtable. Por lo tanto, una interfaz dual en un entorno JScript VBScript funciona como una interfaz de distribución.

 

 