---
title: Optimización mediante GetInfoEx
description: Se usa para cargar valores de atributo específicos en la memoria caché local desde el servicio de directorio subyacente.
ms.assetid: e6111957-22cb-4473-9814-5bcbc79583b2
ms.tgt_platform: multiple
keywords:
- Optimización mediante GetInfoEx ADSI
- GetInfoEx ADSI , Optimización mediante los IAD GetInfoEx
- ADSI ADSI , Uso y optimización mediante el método GetInfoEx de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b522093fff00700cf35b864edde2a6ae7f8f9922
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126887089"
---
# <a name="optimization-using-getinfoex"></a>Optimización mediante GetInfoEx

El [**método IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) se usa para cargar valores de atributo específicos en la memoria caché local desde el servicio de directorio subyacente. Este método solo carga los valores de atributo especificados en la memoria caché local. El [**método IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) se usa para cargar todos los valores de atributo en la memoria caché local.

El [**método IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) obtiene valores actuales específicos para las propiedades de un objeto Active Directory del almacén de directorios subyacente, actualizando los valores almacenados en caché.

Sin embargo, si ya existe un valor en la caché de propiedades, al llamar al método [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) o [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) sin llamar primero a [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para ese atributo, se recuperará el valor almacenado en caché en lugar del valor más actual del directorio subyacente. Esto puede hacer que los valores de atributo actualizados se sobrescriban si se ha modificado la memoria caché local, pero los valores no se han confirmado en el servicio de directorio subyacente con una llamada al método [**IADs.SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) El método sugerido para evitar problemas de almacenamiento en caché es confirmar siempre los cambios de valor de atributo llamando a **IADs.SetInfo** antes de llamar a [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).


```VB
Dim usr As IADs
Dim PropArray As Variant

On Error GoTo Cleanup

' Bind to a specific user object.
Set usr = GetObject("LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' The code example assumes that the property description has a single value in the directory.
' Be aware that this will implicitly call GetInfo because, at this point, GetInfo
' has not yet been called (implicitly or explicitly) on the usr object.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Change two of the attribute values in the local cache.
usr.Put "cn", "Jeff Smith"
usr.Put "title", "Vice President"
usr.Put "department", "Head Office"
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

' Initialize the array of properties to pass to GetInfoEx.
PropArray = Array("department", "title")
 
' Get the specified attribute values.
usr.GetInfoEx PropArray, 0

' The specific attributes values were overwritten, but the attribute
' value not retrieved has not changed.
Debug.Print "User's common name is " + usr.Get("cn")
Debug.Print "User's title is " + usr.Get("title")
Debug.Print "User's department is " + usr.Get("department")

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```



## <a name="retrieving-active-directory-constructed-attributes"></a>Recuperar Active Directory atributos construidos

En Active Directory, la mayoría de los atributos construidos se recuperan y almacenan en caché cuando se llama al método [**IADs.GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ([**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) realiza una llamada **implícita a IADs.GetInfo** si la memoria caché está vacía). Sin embargo, algunos atributos construidos no se recuperan y almacenan en caché automáticamente y, por lo tanto, requieren que se llame explícitamente al método [**IADs.GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para recuperarlos. Por **\_ \_ \_ \_ ejemplo,** en Active Directory, el atributo [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname) no se recupera cuando se llama al método **IADs.GetInfo** y **IADs.Get** devolverá E ADS PROPERTY NOT FOUND . Se **debe llamar al método IADs.GetInfoEx** para recuperar el atributo **canonicalName.** Estos mismos atributos construidos tampoco se recuperarán mediante la [**interfaz IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) para enumerar los atributos.

Para obtener más información y un ejemplo de código que muestra cómo recuperar todos los valores de atributo, vea Código de ejemplo [para leer un atributo construido](example-code-for-reading-a-constructed-attribute.md).

 

 