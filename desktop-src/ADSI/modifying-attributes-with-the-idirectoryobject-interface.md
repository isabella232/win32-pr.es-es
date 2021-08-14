---
title: Modificar atributos con la interfaz IDirectoryObject
description: Además de los ID Put e IAD PutEx, puede usar el método SetObjectAttributes de IDirectoryObject para modificar los valores de atributo. Para usar este método, debe rellenar una estructura \_ ADS ATTR \_ INFO para cada atributo que se va a modificar.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Modificar atributos con el ADSI de la interfaz IDirectoryObject
- IDirectoryObject ADSI , Usar para modificar atributos
- ADSI ADSI, código de ejemplo C/C++ , uso de IDirectoryObject para modificar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fa7d75d3e0dce489f676dafb36992c95a1cba2e9856bbbaf49f14806a6c1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179033"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Modificar atributos con la interfaz IDirectoryObject

Además de [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utEx,**](/windows/desktop/api/Iads/nf-iads-iads-putex)puede usar el método [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) para modificar los valores de atributo. Para usar este método, debe rellenar una estructura [**\_ ADS ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo que se va a modificar.

El [**método IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) permite modificar atributos con un solo valor y con varios valores. Esta función proporciona controles operativos similares, como clear, append, delete y update, a los que se encuentran en el método [**IADs::P utEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Las constantes de control incluyen:

-   [**ADS \_ ATTR \_ CLEAR**](adsi-attribute-modification-types.md)
-   [**ACTUALIZACIÓN \_ DE ATTR de \_ ADS**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ APPEND**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ DELETE**](adsi-attribute-modification-types.md)

Si se especifica [**ADS \_ ATTR \_ UPDATE,**](adsi-attribute-modification-types.md) se desencadenará una operación del lado servidor que puede hacer un uso intensivo de recursos. Un ejemplo sería iniciar la operación para actualizar una larga lista de pertenencia a grupos. En general, evite usar esta operación a menos que la modificación implique un pequeño número de atributos en el directorio. Para modificar una larga lista de pertenencias a grupos, el enfoque más eficaz sería leer la lista desde el directorio subyacente, realizar modificaciones y volver a almacenar la lista actualizada en el directorio.

> [!Note]  
> Al igual que [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs::P utEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) con [**IADs::SetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)los cambios de atributo se confirman o descartan completamente en Active Directory. Si no se permiten una o varias de las modificaciones y, por tanto, no se pueden realizar, ninguna de las modificaciones colectivas realizadas en los atributos se confirma en el directorio.

 

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo modificar atributos únicos y con varios valores con el [**método IDirectoryObject::SetObjectAttributes.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)


```C++
HRESULT hr;
LPCWSTR pwszADsPath = L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com";
IDirectoryObject *pDirObject = NULL;

// Bind to the object.
hr = ADsGetObject(pwszADsPath, IID_IDirectoryObject, (void**)&pDirObject);
if(SUCCEEDED(hr))
{ 
    ADSVALUE adsvFaxNumber;
    ADSVALUE rgadsvOtherTelephones[2];
     
    // Set the new FAX number.
    adsvFaxNumber.dwType = ADSTYPE_CASE_IGNORE_STRING; 
    adsvFaxNumber.CaseIgnoreString = L"425-707-9790";

    // Set the first telephone number.
    rgadsvOtherTelephones[0].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[0].CaseIgnoreString = L"425-707-9791";

    // Set the second telephone number.
    rgadsvOtherTelephones[1].dwType = ADSTYPE_CASE_IGNORE_STRING;
    rgadsvOtherTelephones[1].CaseIgnoreString = L"425-707-9792";

    ADS_ATTR_INFO attrInfo[2];

    // Setup the facsimileTelephoneNumber attribute data.
    attrInfo[0].pszAttrName = L"facsimileTelephoneNumber";
    attrInfo[0].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[0].dwADsType = adsvFaxNumber.dwType;
    attrInfo[0].pADsValues = &adsvFaxNumber;
    attrInfo[0].dwNumValues = 1;

    // Setup the otherTelephone attribute data.
    attrInfo[1].pszAttrName = L"otherTelephone";
    attrInfo[1].dwControlCode = ADS_ATTR_UPDATE;
    attrInfo[1].dwADsType = rgadsvOtherTelephones[0].dwType;
    attrInfo[1].pADsValues = rgadsvOtherTelephones;
    attrInfo[1].dwNumValues = sizeof(rgadsvOtherTelephones)/sizeof(ADSVALUE);

    DWORD dwReturn;
 
    // Set the new attribute values.
    hr = pDirObject->SetObjectAttributes(attrInfo, 
        sizeof(attrInfo)/sizeof(ADS_ATTR_INFO), 
        &dwReturn);

    pDirObject->Release();
}
```



 

 




