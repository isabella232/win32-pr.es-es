---
title: Enumerar objetos
description: Para ver el objeto secundario de un contenedor, como una unidad organizativa (OU), enumere el objeto contenedor.
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- Enumerar objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903062"
---
# <a name="enumerating-objects"></a>Enumerar objetos

Para ver el objeto secundario de un contenedor, como una unidad organizativa (OU), enumere el objeto contenedor. Para crear una analogía con un sistema de archivos, el objeto secundario se corresponderá con los archivos del directorio, mientras que el contenedor, que es el objeto primario, se corresponderá con el propio directorio. También puede usar la operación enumerar cuando desee obtener el objeto primario de un objeto.

Al enumerar un objeto, realmente se enlaza a un objeto en el directorio y se devuelve una interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) en cada objeto.

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



Puede filtrar los tipos de objetos devueltos por la enumeración. Por ejemplo, para mostrar solo usuarios y grupos, use el siguiente ejemplo de código antes de la enumeración.


```VB
Ou.Filter = Array("user", "group")
```



Si tiene una referencia de objeto, puede obtener el elemento primario del objeto mediante la propiedad [**primaria**](iads-property-methods.md) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . En el ejemplo de código siguiente se muestra cómo enlazar al objeto primario.


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



Para obtener más información, consulte [enumeración de objetos ADSI](enumerating-adsi-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Buscar objetos](searching-for-objects.md)
</dt> </dl>

 

 




