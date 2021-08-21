---
title: Código de ejemplo para mover un objeto
description: En este tema se incluyen ejemplos de código que se usan para mover un objeto en el dominio.
ms.assetid: 6a54543b-c6e7-486f-afd1-5380e8a8b727
ms.tgt_platform: multiple
keywords:
- Código de ejemplo para mover un ad de objeto
- Active Directory ejemplos Active Directory , mover un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f3c32f9bf00d96c42a6c7e019852b80b0e30654d7ff03af539b5196349c48ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118693389"
---
# <a name="example-code-for-moving-an-object"></a>Código de ejemplo para mover un objeto

En este tema se incluyen ejemplos de código que se usan para mover un objeto en el dominio.

En el siguiente ejemplo de código de C++ se muestra cómo usar ADSI para mover un objeto en el dominio.


```C++
#include <stdio.h>
#include <atlbase.h>
#include <activeds.h>
#include <ntldap.h>

/***************************************************************************

    MoveObject()

    Moves an object in the directory.

    Parameters:

    padsToMove - Contains an IADs interface pointer that represents the 
    object to move.
    
    padsDestination - Contains an IADs interface pointer that represents the 
    container to move the object to.

***************************************************************************/

HRESULT MoveObject(IADs *padsToMove, IADs *padsDestination)
{
    _ASSERT(padsToMove);
    _ASSERT(padsDestination);
    
    HRESULT hr;
 
    // Get the ADsPath of the object to move.
    CComBSTR sbstrPathToMove;
    hr = padsToMove->get_ADsPath(&sbstrPathToMove); 
    if(FAILED(hr))
    {
        return hr;
    }
    
    // Get an IADsContainer instance from the destination.
    CComPtr<IADsContainer> spContainerDestination;
    hr = padsDestination->QueryInterface(IID_IADsContainer, (void**)&spContainerDestination);
    if(FAILED(hr))
    {
        return hr;
    }

    // Move the object.
    CComPtr<IDispatch> spDispNewObject;
    hr = spContainerDestination->MoveHere(sbstrPathToMove, NULL, &spDispNewObject);

    return hr;
}
```



En el Visual Basic ejemplo de código siguiente se muestra cómo usar ADSI para mover un objeto en el dominio.


```VB
''''''''''''''''''''''''''''''''''''''''
'
'   MoveObject
'
'   Moves an object in the directory.
'
'   Parameters:
'
'   DNToMove - Contains the distinguished name of the object to move.
'
'   DNDestination - Contains the distinguished name of the destination
'   container.
'
''''''''''''''''''''''''''''''''''''''''
Public Sub MoveObject(DNToMove As String, DNDestination As String)
    Dim oContainer As IADsContainer
    
    ' Bind to the destination container.
    Set oContainer = GetObject("LDAP://" & DNDestination)
    
    oContainer.MoveHere "LDAP://" & DNToMove, vbNullString
End Sub
```



 

 




