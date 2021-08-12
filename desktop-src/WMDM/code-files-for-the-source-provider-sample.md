---
title: Archivos de código para el ejemplo de proveedor de origen
description: Archivos de código para el ejemplo de proveedor de origen
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Media Administrador de dispositivos,samples
- Administrador de dispositivos,samples
- Windows Ejemplo Administrador de dispositivos, proveedor de servicios
- Administrador de dispositivos,ejemplo de proveedor de servicios
- proveedores de servicios, ejemplos
- samples,service providers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c29127aebea6898868b29adb17a15c8d174e1fedfd3228bd565bf8ef4ce9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118586372"
---
# <a name="code-files-for-the-source-provider-sample"></a>Archivos de código para el ejemplo de proveedor de origen

El proyecto de proveedor de origen de ejemplo incluye los siguientes archivos de código fuente, con encabezados asociados:



| Archivo                   | Descripción                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch.cpp            | Incluye archivos ATL estándar.                                                                                                                                                                                    |
| key.c                  | Contiene una clave de autenticación ficticia.                                                                                                                                                                            |
| loghelp.cpp            | Contiene funciones que registra la actividad y los errores mediante la **clase WMDMLogger,** que se implementa en el WMDMLOG.dll del sistema.                                                                         |
| MDServiceProvider.cpp  | Implementa una clase, CMDServiceProvider, que implementa las interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) e IComponentAuthenticate.                                                             |
| mdsp.cpp               | Punto de entrada y código de registro de DLL.                                                                                                                                                                          |
| MDSPDevice.cpp         | Implementa una clase, CMDSPDevice, que implementa las interfaces [**IMDSPDevice2,**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2) [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)e **ISpecifyPropertyPages.**                          |
| MDSPEnumDevice.cpp     | Implementa una clase, CMDSPEnumDevice, que implementa la [**interfaz IMDSPEnumDevice.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)                                                                                                  |
| MDSPEnumStorage.cpp    | Implementa una clase, CMDSPEnumStorage, que implementa la [**interfaz IMDSPEnumStorage.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)                                                                                               |
| MDSPStorage.cpp        | Implementa una clase, CMDSPStorage, que implementa las interfaces [**IMDSPStorage2,**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2) [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)e [**IMDSPObject.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject)                    |
| MDSPStorageGlobals.cpp | Implementa una clase, CMDSPStorageGlobals, que implementa la [**interfaz IMDSPStorageGlobals.**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals)                                                                                      |
| MDSPutil.cpp           | Contiene varias funciones de utilidad para la administración de dispositivos y archivos.                                                                                                                                              |
| proppage.cpp           | Implementa una clase, CPropPage, que hereda las clases ATL **IPropertyPageImpl** (para implementar IPropertyPage) y **CDialogImpl**, que hereda la clase ATL CDialogImpl (para administrar ventanas y mensajes). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Proveedor de servicios de ejemplo**](sample-service-provider.md)
</dt> </dl>

 

 




