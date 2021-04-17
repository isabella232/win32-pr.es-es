---
title: Interfaz IWMDRMDeviceApp2
description: La interfaz IWMDRMDeviceApp2 extiende IWMDRMDeviceApp proporcionando una nueva versión del método QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interfaz IWMDRMDeviceApp2 Administrador de dispositivos de Windows Media
- Interfaz IWMDRMDeviceApp2 de Windows Media Administrador de dispositivos, se describe
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358305"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interfaz IWMDRMDeviceApp2

La interfaz **IWMDRMDeviceApp2** extiende [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) proporcionando una nueva versión del método [**QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) . **QueryDeviceStatus2** permite al autor de la llamada consultar un requisito específico de DRM.

Para obtener esta interfaz, llame a **CoCreateInstance** y pase CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Esta interfaz se define en el archivo de encabezado generado a partir de WMDRMDeviceApp. idl. Este encabezado **\# incluye** "WMDM. h". Es posible que deba cambiar este nombre de archivo para que coincida con el encabezado generado a partir de WMDM. idl.

 

## <a name="members"></a>Miembros

La interfaz **IWMDRMDeviceApp2** hereda de [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMDeviceApp2** tiene estos métodos.



| Método                                                            | Descripción                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Consulta un dispositivo para una funcionalidad o estado DRM específico.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicaciones**](interfaces-for-applications.md)
</dt> <dt>

[**Uso del contenido de disponibilidad**](metering-content-usage.md)
</dt> </dl>

 

 





