---
title: Registro del servicio de texto
description: Además de las entradas del registro del servidor COM en proceso estándar, un servicio de texto debe registrarse en el marco de trabajo de servicios de texto (TSF) para que pueda estar disponible para su uso con una aplicación.
ms.assetid: 95676067-ab5c-470b-a4be-117ab6810d48
keywords:
- Text Services Framework (TSF), registro
- TSF (marco de trabajo de servicios de texto), registro
- servicios de texto, registro
- Marco de trabajo de servicios de texto (TSF), perfiles de idioma
- TSF (marco de trabajo de servicios de texto), perfiles de idioma
- servicios de texto, perfiles de idioma
- Text Services Framework (TSF), categorías
- TSF (marco de trabajo de servicios de texto), categorías
- servicios de texto, categorías
- registrando servicios de texto
- registrando perfiles de idioma
- registrar categorías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc1b91ad1a3b1fde9a2e49b92950ce2db4876f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487975"
---
# <a name="text-service-registration"></a>Registro del servicio de texto

Además de las entradas del registro del servidor COM en proceso estándar, un servicio de texto debe registrarse en el marco de trabajo de servicios de texto (TSF) para que pueda estar disponible para su uso con una aplicación. TSF proporciona la interfaz [ITfInputProcessorProfiles](/windows/desktop/api/msctf/nn-msctf-itfinputprocessorprofiles) y [ITfCategoryMgr](/windows/desktop/api/msctf/nn-msctf-itfcategorymgr) para simplificar el proceso de registro.

Los proveedores de servicios de texto también deben proporcionar firmas digitales con sus ejecutables binarios. Vea [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)).

## <a name="registering-the-text-service"></a>Registrar el servicio de texto

Un servicio de texto se registra a sí mismo con TSF mediante una llamada a [ITfInputProcessorProfiles:: Register](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-register) con el identificador de clase del servicio de texto. Una instancia de la interfaz **ITfInputProcessorProfiles** se obtiene llamando a **COCREATEINSTANCE** con el CLSID \_ TF \_ InputProcessorProfiles.

En el ejemplo siguiente se muestra cómo crear un objeto **ITfInputProcessorProfiles** y registrar el servicio de texto.


```C++
BOOL RegisterTextService(CLSID clsidTextService)
{
    HRESULT hr;
    ITfInputProcessorProfiles *pInputProcessProfiles;

    hr = CoCreateInstance(  CLSID_TF_InputProcessorProfiles, 
                            NULL, 
                            CLSCTX_INPROC_SERVER,
                            IID_ITfInputProcessorProfiles, 
                            (LPVOID*)&pInputProcessProfiles);

    if (hr != S_OK)
    {
        return FALSE;
    }

    hr = pInputProcessProfiles->Register(clsidTextService);

    pInputProcessProfiles->Release();
    
    return (S_OK == hr);
}
```



[ITfInputProcessorProfiles:: unregister](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-unregister)

## <a name="registering-language-profiles"></a>Registrando perfiles de idioma

Un servicio de texto solo está disponible cuando una aplicación tiene el foco y se selecciona el idioma adecuado en la barra de idioma. Para facilitar esto, TSF requiere que un servicio de texto se registre en todos los idiomas que admite. El servicio de texto registra sus perfiles de lenguaje mediante una llamada a [ITfInputProcessorProfiles:: AddLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-addlanguageprofile) con el identificador de clase de servicio de texto, ese identificador de idioma del perfil y un **GUID** definido por el servicio de texto que identifica el perfil de idioma.

Un perfil de idioma se puede quitar llamando a [ITfInputProcessorProfiles:: RemoveLanguageProfile](/windows/desktop/api/msctf/nf-msctf-itfinputprocessorprofiles-removelanguageprofile). **ITfInputProcessorProfiles:: unregister** quita todos los perfiles de lenguaje para el servicio de texto; Cuando se desinstala un servicio de texto, requiere la eliminación de los perfiles de idioma individuales.

## <a name="registering-categories"></a>Registrar categorías

Un servicio de texto también debe registrar la categoría a la que se aplica el servicio de texto. Por ejemplo, si el servicio de texto proporciona información de atributos de visualización, debe registrarse como un proveedor de atributos para mostrar llamando a [ITfCategoryMgr:: RegisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registercategory) con el identificador de clase del servicio de texto para el primer parámetro, GUID \_ TFCAT \_ DISPLAYATTRIBUTEPROVIDER para el segundo parámetro y el identificador de clase del servicio de texto de nuevo para el tercer parámetro. Las categorías posibles se enumeran en [valores de categoría predefinidos](predefined-category-values.md).

Quite las categorías previamente registradas llamando a [ITfCategoryMgr:: UnregisterCategory](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-unregistercategory). ITfInputProcessorProfiles:: unregister quita todas las categorías para el servicio de texto; Cuando se desinstala un servicio de texto, debe quitar las categorías individuales.

 

 