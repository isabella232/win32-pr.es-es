---
title: Interfaz IWMDRMDeviceApp2
description: La interfaz IWMDRMDeviceApp2 amplía IWMDRMDeviceApp proporcionando una nueva versión del método QueryDeviceStatus.
ms.assetid: a7e28d5a-041f-4102-97db-0c77ca146e26
keywords:
- Interfaz IWMDRMDeviceApp2 windows Media Administrador de dispositivos
- Interfaz IWMDRMDeviceApp2 windows Media Administrador de dispositivos , descrito
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17bd0d7aa729103a81fca6732ed178ac5ced583566dd353a28716d4933e602ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584499"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interfaz IWMDRMDeviceApp2

La **interfaz IWMDRMDeviceApp2** amplía [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) proporcionando una nueva versión del [**método QueryDeviceStatus.**](iwmdrmdeviceapp-querydevicestatus.md) **QueryDeviceStatus2 permite** al autor de la llamada consultar un requisito específico de DRM.

Para obtener esta interfaz, llame **a CoCreateInstance** y pase CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Esta interfaz se define en el archivo de encabezado creado a partir de WMDRMDeviceApp.idl. Este encabezado **\# incluye** "wmdm.h". Es posible que tenga que cambiar este nombre de archivo para que coincida con el encabezado creado a partir de WMDM.idl.

 

## <a name="members"></a>Miembros

La **interfaz IWMDRMDeviceApp2** hereda de [**IWMDRMDeviceApp.**](iwmdrmdeviceapp.md) **IWMDRMDeviceApp2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMDeviceApp2** tiene estos métodos.



| Método                                                            | Descripción                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Consulta un dispositivo para un estado o funcionalidad específicos de DRM.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Control del contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicaciones**](interfaces-for-applications.md)
</dt> <dt>

[**Uso de contenido de medición**](metering-content-usage.md)
</dt> </dl>

 

 





