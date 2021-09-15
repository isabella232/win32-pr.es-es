---
title: Protección de archivos con DRM versión 1
description: Protección de archivos con DRM versión 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows SDK de formato multimedia, creación de archivos protegidos
- Windows SDK de formato multimedia, archivos protegidos
- Formato de sistemas avanzados (ASF), crear archivos protegidos
- ASF (formato de sistemas avanzados), crear archivos protegidos
- Formato de sistemas avanzados (ASF), archivos protegidos
- ASF (formato de sistemas avanzados), archivos protegidos
- Formato de sistemas avanzados (ASF),WMStubDRM.lib
- ASF (formato de sistemas avanzados),WMStubDRM.lib
- WMStubDRM.lib, crear archivos protegidos
- WMStubDRM.lib,archivos protegidos
- administración de derechos digitales (DRM),WMStubDRM.lib
- DRM (administración de derechos digitales),WMStubDRM.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466689"
---
# <a name="protecting-files-with-drm-version-1"></a>Protección de archivos con DRM versión 1

Cuando se aplica este tipo de protección, se genera una licencia DRM versión 1 que solo es válida en la máquina desde la que se realizó la solicitud de licencia. Dado que no se establece ninguna clave o valor de ed. de clave, no hay ninguna manera de generar licencias portables para el contenido protegido mediante esta técnica. Sin embargo, al usar Windows SDK de formato multimedia 7.1 o posterior, las licencias se pueden recuperar en Microsoft License Migration Service.

Para proteger los archivos ASF mediante DRM versión 1, realice los pasos siguientes:

1.  Vincule el archivo WMStubDRM.lib al proyecto y, si es necesario, desvincule wmvcore.lib.
2.  Llame a [**la función WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) para crear el escritor. El primer argumento está reservado y debe establecerse en **NULL.**
3.  Establezca un perfil para que el escritor lo use mediante una llamada a [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid). Debe establecer un perfil en el sistema de escritura antes de establecer los atributos DRM. DRM solo se admite para los perfiles que usan los códecs Windows Audio multimedia o Windows de vídeo multimedia.
4.  Con el [**método IWMHeaderInfo::SetAttribute,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) establezca las siguientes propiedades DRM. La **propiedad \_ Usar DRM** indica a los componentes de DRM que protejan el contenido mediante DRM versión 1. La **propiedad \_ Marcas** DRM especifica los derechos que se incluirán en la licencia local que se creará para el contenido. El **valor \_ DE NIVEL** DE DRM también se almacena en la licencia; especifica el nivel mínimo necesario para acceder al contenido. 150 es el nivel recomendado para el contenido de la versión 1 de DRM.

    | Atributo      | Value                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | **Uso de \_ DRM**   | **TRUE**                                                                                    |
    | **Marcas \_ DRM** | WMT \_ RIGHT \_ PLAYBACK \| WMT \_ RIGHT \_ COPY \_ TO \_ NON \_ SDMI \_ DEVICE \| WMT \_ RIGHT \_ COPY \_ TO \_ CD |
    | **NIVEL DE \_ DRM** | 150                                                                                         |

    

     

En el código de ejemplo siguiente se muestra cómo crear un sistema de escritura habilitado para DRM para DRM versión 1 y establecer las propiedades de DRM. Se ha omitido la comprobación de errores para aclararlo.


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



 

 




