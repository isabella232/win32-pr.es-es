---
title: Modificar atributos con la interfaz IDirectoryObject
description: Además de IADs Put y IADs PutEx, puede usar el método IDirectoryObject SetObjectAttributes para modificar los valores de atributo. Para usar este método, debe rellenar una \_ \_ estructura de información de atributos de ADS para modificar cada atributo.
ms.assetid: 1d3fe8f6-34be-4bcb-8ba5-2d92ddc0852a
ms.tgt_platform: multiple
keywords:
- Modificar atributos con la interfaz IDirectoryObject ADSI
- IDirectoryObject ADSI, usar para modificar atributos
- ADSI ADSI, código de ejemplo C/C++, uso de IDirectoryObject para modificar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715826d0fc835f3d9ecae914fcc51603883af5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148734"
---
# <a name="modifying-attributes-with-the-idirectoryobject-interface"></a>Modificar atributos con la interfaz IDirectoryObject

Además de [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) y [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex), puede utilizar el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) para modificar los valores de atributo. Para usar este método, debe rellenar una estructura de [**\_ \_ información de atributos de ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para modificar cada atributo.

El método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) permite modificar los atributos de un solo valor y de varios valores. Esta función proporciona controles operativos similares, como Clear, append, delete y Update, a los que se encuentran en el método [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Las constantes de control incluyen:

-   [**\_claridad del atributo ADS \_**](adsi-attribute-modification-types.md)
-   [**\_actualización de atributos de ADS \_**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ Append**](adsi-attribute-modification-types.md)
-   [**ADS \_ ATTR \_ eliminar**](adsi-attribute-modification-types.md)

Si se especifica, la [**\_ \_ actualización del atributo ADS**](adsi-attribute-modification-types.md) desencadenará una operación del lado servidor que puede consumir muchos recursos. Un ejemplo sería iniciar la operación para actualizar una larga lista de pertenencia a grupos. En general, no se debe usar esta operación a menos que la modificación implique un pequeño número de atributos en el directorio. Para modificar una larga lista de pertenencias a grupos, el enfoque más eficaz sería leer la lista del directorio subyacente, realizar modificaciones y volver a almacenar la lista actualizada en el directorio.

> [!Note]  
> Como [**IADs::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put) y [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) con [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), los cambios de atributo se confirman por completo o se descartan en Active Directory. Si una o varias de las modificaciones no se permiten y, por lo tanto, no se pueden realizar, ninguna de las modificaciones colectivas realizadas en los atributos se confirman en el directorio.

 

## <a name="example"></a>Ejemplo

En el ejemplo de código siguiente se muestra cómo modificar los atributos únicos y con varios valores con el método [**IDirectoryObject:: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .


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



 

 




