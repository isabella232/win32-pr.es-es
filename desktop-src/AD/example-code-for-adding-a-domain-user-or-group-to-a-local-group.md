---
title: Código de ejemplo para agregar un usuario o grupo de dominio a un grupo local
description: En este tema se incluye un ejemplo de código que muestra cómo agregar un usuario o grupo de dominio a un grupo local en un servidor miembro o un equipo que se ejecuta en Windows NT Workstation o Windows 2000 Professional.
ms.assetid: 6333ce9f-0396-4af7-9e81-f008cf4536ec
ms.tgt_platform: multiple
keywords:
- Active Directory ejemplos Active Directory, agregar un usuario o grupo de dominio a un grupo local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539e8fbbeed3d865a0878236745b7a3c74c76d27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773219"
---
# <a name="example-code-for-adding-a-domain-user-or-group-to-a-local-group"></a><span data-ttu-id="e9f1b-104">Código de ejemplo para agregar un usuario o grupo de dominio a un grupo local</span><span class="sxs-lookup"><span data-stu-id="e9f1b-104">Example Code for Adding a Domain User or Group to a Local Group</span></span>

<span data-ttu-id="e9f1b-105">El siguiente ejemplo de código de C++ agrega un usuario o grupo de dominio a un grupo local en un servidor miembro o un equipo que se ejecuta en Windows NT Workstation o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e9f1b-105">The following C++ code example adds a domain user or group to a local group on a member server or a computer running on Windows NT Workstation or Windows 2000 Professional.</span></span>


```C++
#include <stdio.h>
#include <atlbase.h>
#include <activeds.h>
#include <ntldap.h>

/*******************************************************************

    AddDomainUserToLocalGroup()

    Adds a user from a domain to a local group using the WinNT 
    provider.

    Parameters:

    pwszComputerName - Contains the name of the computer 
    that the group belongs to.

    pwszGroupName - Contains the name of the group to add a member 
    to. This group must exist on the target computer.

    pwszDomainName - Contains the name of domain that contains 
    the user to add to the group.

    pwszUserToAdd - Contains the name of the user in the domain 
    to add to the group.

*******************************************************************/

HRESULT AddDomainUserToLocalGroup(LPCWSTR pwszComputerName, 
                                  LPCWSTR pwszGroupName, 
                                  LPCWSTR pwszDomainName, 
                                  LPCWSTR pwszUserToAdd)
{
    HRESULT hr = E_FAIL;
    CComPtr<IADsContainer> spComputer;

    // Build the binding string.
    CComBSTR sbstrBindingString;
    sbstrBindingString = "WinNT://";
    sbstrBindingString += pwszComputerName;
    sbstrBindingString += ",computer";
    
    // Bind to the computer that contains the group.
    hr = ADsOpenObject( sbstrBindingString,
                        NULL, 
                        NULL, 
                        ADS_SECURE_AUTHENTICATION,
                        IID_IADsContainer, 
                        (void**)&spComputer);

    if(FAILED(hr))
    {
        return hr;
    }

    // Bind to the group object.
    CComPtr<IDispatch> spDisp;
    hr = spComputer->GetObject(CComBSTR("group"), 
                               CComBSTR(pwszGroupName), 
                               &spDisp);
    if(FAILED(hr))
    {
        return hr;
    }

    CComPtr<IADsGroup> spGroup;
    hr = spDisp->QueryInterface(IID_IADs, (LPVOID*)&spGroup);
    if(FAILED(hr))
    {
        return hr;
    }
    
    // Bind to the member to add.
    sbstrBindingString = "WinNT://";
    sbstrBindingString += pwszDomainName;
    sbstrBindingString += "/";
    sbstrBindingString += pwszUserToAdd;

    hr = spGroup->Add(sbstrBindingString);

    return hr;
}
```



<span data-ttu-id="e9f1b-106">En el siguiente ejemplo de código Visual Basic se agrega un usuario o grupo de dominio a un grupo local en un servidor miembro o un equipo que se ejecuta en Windows NT Workstation o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="e9f1b-106">The following Visual Basic code example adds a domain user or group to a local group on a member server or a computer running on Windows NT Workstation or Windows 2000 Professional.</span></span>


```VB
''''''''''''''''''''''''''''''''''''''''
'
'   AddDomainUserToLocalGroup
'
'   Adds a user from a domain to a local group using the WinNT 
'   provider.
'
'   Parameters:
'
'   ComputerName - Contains the name of the computer that the group
'   belongs to.
'
'   GroupName - Contains the name of the group to add a member to. 
'   This group must exist on the target computer.
'
'   DomainName - Contains the name of domain that contains the user
'   to add to the group.
'
'   UserName - Contains the name of the user in the domain to add
'   to the group.
'
''''''''''''''''''''''''''''''''''''''''
Public Sub AddDomainUserToLocalGroup(ComputerName As String, _
                                    GroupName As String, _
                                    DomainName As String, _
                                    UserName As String)
    Dim GroupComputer As IADsContainer
    Dim Group As IADsGroup
    
    ' Bind to the computer that contains the group.
    Set GroupComputer = GetObject("WinNT://" & 
                                  ComputerName & 
                                  ",computer")
    
    ' Bind to the group object.
    Set Group = GroupComputer.GetObject("group", GroupName)
    
    ' Add the user to the group.
    Group.Add ("WinNT://" & DomainName & "/" & UserName)
End Sub
```



 

 




