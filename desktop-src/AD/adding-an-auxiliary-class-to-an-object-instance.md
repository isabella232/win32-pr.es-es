---
title: Agregar una clase auxiliar a una instancia de objeto
description: En los siguientes ejemplos de código se muestra cómo usar ADSI y LDAP para agregar dinámicamente una clase auxiliar a una instancia de objeto existente.
ms.assetid: 739dd372-3bda-4d94-8daf-f71e3091cfb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a6b1f61bffe9081350949cccddc70fee83a568
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077572"
---
# <a name="adding-an-auxiliary-class-to-an-object-instance"></a>Agregar una clase auxiliar a una instancia de objeto

En los siguientes ejemplos de código se muestra cómo usar ADSI y LDAP para agregar dinámicamente una clase auxiliar a una instancia de objeto existente. En los ejemplos se supone que una clase auxiliar denominada **Vehicle** se define en el esquema de Active Directory y que la clase **Vehicle** tiene un atributo **Vin** .

Cuando agrega dinámicamente una clase auxiliar a una instancia de objeto, debe especificar simultáneamente los valores de los atributos **mustHave** obligatorios en la clase. En los siguientes ejemplos se muestra cómo hacerlo con el atributo "Vin", que se supone que es obligatorio.

En el siguiente ejemplo de C++ se enlaza a un objeto y se usa [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) para anexar la clase auxiliar a la lista de clases en la propiedad **objectClass** del objeto. A continuación, en el ejemplo se usa [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put) para establecer el valor del atributo **Vin** . Por último, llama a [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) para confirmar los cambios en el directorio.


```C++
LPWSTR pszAuxClass[]={L"vehicle"};
LPWSTR pszVIN[]={L"df897dsfsa-0"};
VARIANT var;

VariantInit(&var);

ADsOpenObject(L"cn=johnd,cn=users,dc=fabrikam,dc=com", 
    NULL, 
    NULL, 
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,  
    (VOID**)&pIADs);

ADsBuildVarArrayStr(pszAuxClass, 1, &var);
pIADs->PutEx(ADS_PROPERTY_APPEND, CComBSTR("objectClass"), var);
ADsBuildVarArrayStr( pszVIN, 1, &var);
pIADs->Put(CComBSTR("vin"), var);
pIADs->SetInfo();

if(pIADs)
    pIADs->Release();

VariantClear(&var);
```



 

 