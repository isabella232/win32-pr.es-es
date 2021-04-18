---
title: Protección de archivos con DRM versión 1
description: Protección de archivos con DRM versión 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- SDK de Windows Media Format, crear archivos protegidos
- SDK de Windows Media Format, archivos protegidos
- Advanced Systems Format (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Advanced Systems Format (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Advanced Systems Format (ASF), WMStubDRM. lib
- ASF (formato de sistemas avanzados), WMStubDRM. lib
- WMStubDRM. lib, crear archivos protegidos
- WMStubDRM. lib, archivos protegidos
- Administración de derechos digitales (DRM), WMStubDRM. lib
- DRM (administración de derechos digitales), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104358767"
---
# <a name="protecting-files-with-drm-version-1"></a>Protección de archivos con DRM versión 1

Cuando se aplica este tipo de protección, se genera una licencia de DRM versión 1 que solo es válida en el equipo desde el que se realizó la solicitud de licencia. Dado que no se establece ninguna inicialización de clave o clave, no hay ninguna manera de generar licencias portátiles para el contenido protegido con esta técnica. Sin embargo, al usar el SDK de Windows Media Format 7,1 o posterior, las licencias se pueden recuperar en el servicio de migración de licencias de Microsoft.

Para proteger los archivos ASF con DRM versión 1, realice los pasos siguientes:

1.  Vincule el archivo WMStubDRM. lib al proyecto y, si es necesario, desvincule wmvcore. lib.
2.  Llame a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para crear el escritor. El primer argumento está reservado y debe establecerse en **null**.
3.  Establezca un perfil para que lo use el escritor llamando a [**IWMWriter:: SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Debe establecer un perfil en el escritor antes de establecer cualquier atributo DRM. DRM solo es compatible con los perfiles que usan los códecs Windows Media Audio o Windows Media Video.
4.  Con el método [**IWMHeaderInfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , establezca las siguientes propiedades de DRM. La propiedad **usar \_ DRM** indica a los componentes de DRM que protejan el contenido mediante DRM versión 1. La **propiedad \_ marcas DRM** especifica los derechos que se van a incluir en la licencia local que se creará para el contenido. El valor de **\_ nivel DRM** también se almacena en la licencia; especifica el nivel mínimo necesario para tener acceso al contenido. 150 es el nivel recomendado para el contenido de la versión 1 de DRM.

    | Atributo      | Value                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Usar \_ DRM**   | **TRUE**                                                                                    |
    | **\_Marcas DRM** | la \_ reproducción de la \_ \| \_ \_ \_ \_ \_ \_ \| \_ \_ \_ \_ caja derecha de WMT y la copia correcta en el dispositivo no de SDMI. |
    | **nivel de DRM \_** | 150                                                                                         |

    

     

En el ejemplo de código siguiente se muestra cómo crear un escritor habilitado para DRM para DRM versión 1 y cómo establecer las propiedades de DRM. La comprobación de errores se ha omitido por motivos de claridad.


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




