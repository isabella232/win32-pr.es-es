---
title: Archivos de código para el ejemplo de proveedor de origen
description: Archivos de código para el ejemplo de proveedor de origen
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de proveedor de servicios
- Administrador de dispositivos, ejemplo de proveedor de servicios
- proveedores de servicios, ejemplos
- ejemplos, proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148815"
---
# <a name="code-files-for-the-source-provider-sample"></a>Archivos de código para el ejemplo de proveedor de origen

El proyecto de proveedor de origen de ejemplo incluye los siguientes archivos de código fuente, con encabezados asociados:



| Archivo                   | Descripción                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hdsppch. cpp            | Incluye archivos ATL estándar.                                                                                                                                                                                    |
| clave. c                  | Contiene una clave de autenticación ficticia.                                                                                                                                                                            |
| loghelp. cpp            | Contiene funciones que registran la actividad y los errores mediante la clase **WMDMLogger** , que se implementa en el archivo de sistema WMDMLOG.dll.                                                                         |
| MDServiceProvider. cpp  | Implementa una clase, CMDServiceProvider, que implementa las interfaces [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) y IComponentAuthenticate.                                                             |
| mdsp. cpp               | Código de registro y punto de entrada de DLL.                                                                                                                                                                          |
| MDSPDevice. cpp         | Implementa una clase, CMDSPDevice, que implementa las interfaces [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)y **ISpecifyPropertyPages** .                          |
| MDSPEnumDevice. cpp     | Implementa una clase, CMDSPEnumDevice, que implementa la interfaz [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) .                                                                                                  |
| MDSPEnumStorage. cpp    | Implementa una clase, CMDSPEnumStorage, que implementa la interfaz [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) .                                                                                               |
| MDSPStorage. cpp        | Implementa una clase, CMDSPStorage, que implementa las interfaces [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)y [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) .                    |
| MDSPStorageGlobals. cpp | Implementa una clase, CMDSPStorageGlobals, que implementa la interfaz [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) .                                                                                      |
| MDSPutil. cpp           | Contiene varias funciones de utilidad para la administración de dispositivos y archivos.                                                                                                                                              |
| PropPage. cpp           | Implementa una clase, CPropPage, que hereda las clases ATL **IPropertyPageImpl** (para implementar IPropertyPage) y **CDialogImpl**, que hereda la clase de ATL CDialogImpl (para administrar mensajes y ventanas). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Proveedor de servicios de ejemplo**](sample-service-provider.md)
</dt> </dl>

 

 




