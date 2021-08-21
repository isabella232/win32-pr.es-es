---
title: Enlace con ADsOpenObject e IADsOpenDSObject OpenDSObject
description: La función ADsOpenObject y el método OpenDSObject IADsOpenDSObject se usan para enlazar a objetos de servicio de directorio cuando se deben especificar credenciales alternativas y cuando se requiere cifrado de datos.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Enlace con ADsOpenObject e IADsOpenDSObject OpenDSObject ADSI
- ADSI ADSI, mediante, enlace con ADsOpenObject e IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41ffe1e9ad0b8a78d1a8c563de250851a894012938682c4cfd0d0fd713f99bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082779"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Enlace con ADsOpenObject e IADsOpenDSObject::OpenDSObject

La [**función ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y el método [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) se usan para enlazar a objetos de servicio de directorio cuando se deben especificar credenciales alternativas y cuando se requiere cifrado de datos.

Las credenciales del subproceso que realiza la llamada se deben usar siempre que sea posible. Sin embargo, si se deben usar credenciales alternativas, se debe usar la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o el [**método IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) Si se usan credenciales alternativas, es importante no almacenar en caché la contraseña. Se pueden realizar varias operaciones de enlace especificando el nombre de usuario y la contraseña para la primera operación de enlace y, a continuación, especificando solo el nombre de usuario en los siguientes enlaces. El sistema configura una sesión en la primera llamada y usa la misma sesión en las llamadas de enlace posteriores siempre que se cumplen las condiciones siguientes:

-   El mismo nombre de usuario en cada operación de enlace.
-   Implemente el enlace sin servidor o enlace al mismo servidor en cada operación de enlace.
-   Mantenga una sesión abierta manteniendo en una referencia de objeto una de las operaciones de enlace. La sesión se cierra cuando se libera la última referencia de objeto.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) e [**IADsOpenDSObject::OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) usan las interfaces del proveedor de compatibilidad de seguridad [(SSPI)](/windows/desktop/SecAuthN/sspi) de Windows NT para permitir flexibilidad en las opciones de autenticación. La principal ventaja de usar estas interfaces es proporcionar diferentes tipos de autenticación para Active Directory clientes y cifrar la sesión. Actualmente, ADSI no permite que se pasen certificados. Por lo tanto, puede usar SSL para el cifrado y, a continuación, Kerberos, NTLM o autenticación simple, en función de cómo se establezcan las marcas en el *parámetro dwReserved.*

No se puede solicitar un proveedor de SSPI específico en ADSI, aunque siempre se obtiene el protocolo de preferencias más alto. En el caso de un Windows de cliente a un equipo que ejecuta Windows, el protocolo es Kerberos. No permitir un certificado para la autenticación es aceptable en el caso de una página web porque la autenticación se produce antes de ejecutar la página web.

Aunque las operaciones open le permiten especificar un usuario y una contraseña, no debe hacerlo. En su lugar, no especifique ninguna credencial y use implícitamente las credenciales del contexto de seguridad del autor de la llamada. Para enlazar a un objeto de directorio mediante las credenciales del autor de la llamada con [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject::OpenDSObject,**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)especifique **NULL** para el nombre de usuario y la contraseña.

Por último, para enlazar sin autenticación, use la marca **ADS \_ NO \_ AUTHENTICATION.** Ninguna autenticación indica que ADSI intenta enlazarse como usuario anónimo al objeto de destino y no realiza ninguna autenticación. Esto equivale a solicitar enlace anónimo en LDAP e indica que todos los usuarios están incluidos en el contexto de seguridad.

Si las marcas de autenticación se establecen en cero, ADSI realiza un enlace simple, enviado como texto no cifrado.

> [!Caution]  
> Si se especifican un nombre de usuario y una contraseña sin especificar marcas de autenticación, el nombre de usuario y la contraseña se transmiten a través de la red en texto no cifrado, lo que es un riesgo de seguridad. No especifique un nombre de usuario y una contraseña sin especificar marcas de autenticación.

 

## <a name="examples"></a>Ejemplos

En el Visual Basic ejemplo de código siguiente se muestra cómo usar el [**método IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



En el siguiente ejemplo de código de C++ se muestra cómo usar la [**función ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)


```C++
IADs *pObject;
HRESULT hr;

hr = ADsOpenObject(L"LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION, 
    IID_IADs,
    (void**)&pObject);
if(SUCCEEDED(hr))
{
    // Use the object.

    // Release the object.
    pObject->Release()
}
```



La [**interfaz IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) también se puede usar en C++, pero duplica la [**función ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)

En el siguiente ejemplo de código de C++ se muestra cómo usar la interfaz [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) para realizar la misma operación de enlace que en el ejemplo de código anterior.


```C++
IADsOpenDSObject *pDSO;
HRESULT hr;
 
hr = ADsGetObject(L"LDAP:", IID_IADsOpenDSObject, (void**)&pDSO);
if(SUCCEEDED(hr))
{
    IDispatch *pDisp;

    hr = pDSO->OpenDSObject(CComBSTR("LDAP://CN=jeffsmith,DC=fabrikam,DC=com"),
        NULL,
        NULL,
        ADS_SECURE_AUTHENTICATION, 
        &pDisp);
    if(SUCCEEDED(hr))
    {
        IADs *pObject;

        hr = pDisp->QueryInterface(IID_IADs, (void**) &pObject);
        if(SUCCEEDED(hr))
        {
            // Use the object.

            // Release the object.
            pObject->Release();
        }

        pDisp->Release();
    }
    
    pDSO->Release();
}
```



 

 