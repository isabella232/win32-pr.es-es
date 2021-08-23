---
title: Enumerar objetos
description: Para ver el objeto secundario de un contenedor, como una unidad organizativa (OU), enumere el objeto contenedor.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerar objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e4bcead2d3fc8f98daeada89cdd10b3ad30bed855563efd89b3eebce8995f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961954"
---
# <a name="enumerating-objects"></a>Enumerar objetos

Para ver el objeto secundario de un contenedor, como una unidad organizativa (OU), enumere el objeto contenedor. Para hacer una analogía con un sistema de archivos, el objeto secundario correspondería a los archivos del directorio, mientras que el contenedor, que es el objeto primario, correspondería al propio directorio. También puede usar la operación de enumeración cuando desee obtener el objeto primario de un objeto .

Al enumerar un objeto, se enlaza realmente a un objeto en el directorio y se devuelve una interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) en cada objeto.

En el ejemplo de código siguiente se muestra cómo enumerar los elementos secundarios de un contenedor.


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



Puede filtrar los tipos de objetos devueltos por la enumeración . Por ejemplo, para mostrar solo usuarios y grupos, use el siguiente ejemplo de código antes de la enumeración .


```VB
Ou.Filter = Array("user", "group")
```



Si tiene una referencia de objeto, puede obtener el elemento primario del objeto mediante la propiedad [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**Parent.**](iads-property-methods.md) En el ejemplo de código siguiente se muestra cómo enlazar al objeto primario.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Para obtener más información, [vea Enumerar objetos ADSI.](enumerating-adsi-objects.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar objetos](searching-for-objects.md)
</dt> </dl>

 

 




