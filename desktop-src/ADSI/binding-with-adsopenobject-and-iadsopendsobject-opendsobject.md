---
title: Enlazar con ADsOpenObject y IADsOpenDSObject OpenDSObject
description: La función ADsOpenObject y el método IADsOpenDSObject OpenDSObject se usan para enlazar con objetos de servicio de directorio cuando se deben especificar credenciales alternativas y cuando se requiere el cifrado de datos.
ms.assetid: 7b8ded11-e04f-40f5-a82a-5972c4df9dea
ms.tgt_platform: multiple
keywords:
- Enlazar con ADsOpenObject y IADsOpenDSObject OpenDSObject ADSI
- ADSI ADSI, usar, enlazar con ADsOpenObject y IADsOpenDSObject OpenDSObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5a249aa3d51520d0d345b5a098f84480e5b5016
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078362"
---
# <a name="binding-with-adsopenobject-and-iadsopendsobjectopendsobject"></a>Enlazar con ADsOpenObject y IADsOpenDSObject:: OpenDSObject

La función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) se usan para enlazar con objetos de servicio de directorio cuando se deben especificar credenciales alternativas y cuando se requiere el cifrado de datos.

Las credenciales del subproceso que realiza la llamada deben usarse cuando sea posible. Sin embargo, si se deben usar credenciales alternativas, se debe usar la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . Si se usan credenciales alternativas, es importante no almacenar en caché la contraseña. Se pueden realizar varias operaciones de enlace especificando el nombre de usuario y la contraseña para la primera operación de enlace y, a continuación, especificando solo el nombre de usuario en los enlaces subsiguientes. El sistema configura una sesión en la primera llamada y usa la misma sesión en las llamadas de enlace subsiguientes siempre que se cumplan las condiciones siguientes:

-   El mismo nombre de usuario en cada operación de enlace.
-   Implemente el enlace sin servidor o enlace al mismo servidor en cada operación de enlace.
-   Mantenga una sesión abierta manteniendo en una referencia de objeto de una de las operaciones de enlace. La sesión se cierra cuando se libera la última referencia de objeto.

[**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) y [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) usan las interfaces del [proveedor de compatibilidad para seguridad (SSPI)](/windows/desktop/SecAuthN/sspi) de Windows NT para ofrecer flexibilidad en las opciones de autenticación. La principal ventaja de utilizar estas interfaces es proporcionar diferentes tipos de autenticación a Active Directory clientes y cifrar la sesión. Actualmente, ADSI no permite que se pasen los certificados. Por lo tanto, puede usar SSL para el cifrado y, después, Kerberos, NTLM o autenticación simple, en función de cómo se establezcan las marcas en el parámetro *dwReserved* .

No se puede solicitar un proveedor de SSPI específico en ADSI, aunque siempre se obtiene el protocolo de preferencias más alto. En el caso de un cliente de Windows que se enlaza a un equipo que ejecuta Windows, el protocolo es Kerberos. No permitir un certificado para la autenticación es aceptable en el caso de una página web porque la autenticación se produce antes de ejecutar la Página Web.

Aunque las operaciones de apertura permiten especificar un usuario y una contraseña, no debe hacerlo. En su lugar, no especifique ninguna credencial y use implícitamente las credenciales del contexto de seguridad del llamador. Para enlazar a un objeto de directorio con las credenciales del autor de la llamada con [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject), especifique **null** para el nombre de usuario y la contraseña.

Por último, para enlazar sin autenticación, use la marca **ADS \_ no \_ Authentication** . Sin autenticación indica que ADSI intenta enlazar como un usuario anónimo al objeto de destino y no realiza ninguna autenticación. Esto es equivalente a solicitar un enlace anónimo en LDAP e indica que todos los usuarios están incluidos en el contexto de seguridad.

Si las marcas de autenticación se establecen en cero, ADSI realiza un enlace simple, enviado como texto no cifrado.

> [!Caution]  
> Si se especifica un nombre de usuario y una contraseña sin especificar marcas de autenticación, el nombre de usuario y la contraseña se transmiten por la red en texto sin formato, lo que constituye un riesgo para la seguridad. No especifique un nombre de usuario y una contraseña sin especificar marcas de autenticación.

 

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de código de Visual Basic se muestra cómo usar el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .


```VB
Dim openDS As IADsOpenDSObject
Dim usr As IADsUser
 
Set openDS = GetObject("LDAP:")
 
openDS.OpenDSObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com",
    NULL, 
    NULL,
    ADS_SECURE_AUTHENTICATION)
```



En el ejemplo de código de C++ siguiente se muestra cómo usar la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .


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



La interfaz [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) también se puede usar en C++, pero duplica la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

En el ejemplo de código de C++ siguiente se muestra cómo utilizar la interfaz [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject) para realizar la misma operación de enlace que en el ejemplo de código anterior.


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



 

 