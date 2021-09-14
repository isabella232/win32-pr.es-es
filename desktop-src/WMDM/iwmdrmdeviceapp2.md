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
ms.openlocfilehash: df4bfdb023198631b16ffa0e511488fa52423c5e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890289"
---
# <a name="iwmdrmdeviceapp2-interface"></a>Interfaz IWMDRMDeviceApp2

La **interfaz IWMDRMDeviceApp2** amplía [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) proporcionando una nueva versión del [**método QueryDeviceStatus.**](iwmdrmdeviceapp-querydevicestatus.md) **QueryDeviceStatus2 permite** al autor de la llamada consultar un requisito específico de DRM.

Para obtener esta interfaz, llame **a CoCreateInstance** y pase CLSID \_ WMDRMDeviceApp.

> [!Note]  
> Esta interfaz se define en el archivo de encabezado creado a partir de WMDRMDeviceApp.idl. Este encabezado **\# incluye** "wmdm.h". Es posible que tenga que cambiar este nombre de archivo para que coincida con el encabezado creado a partir de WMDM.idl.

 

## <a name="members"></a>Members

La **interfaz IWMDRMDeviceApp2** hereda de [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md). **IWMDRMDeviceApp2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWMDRMDeviceApp2** tiene estos métodos.



| Método                                                            | Descripción                                                          |
|:------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) | Consulta un dispositivo para obtener un estado o una funcionalidad de DRM específicos.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IWMDRMDeviceApp**](iwmdrmdeviceapp.md)
</dt> <dt>

[**Control de contenido protegido en la aplicación**](handling-protected-content-in-the-application.md)
</dt> <dt>

[**Interfaces para aplicaciones**](interfaces-for-applications.md)
</dt> <dt>

[**Uso de contenido de medición**](metering-content-usage.md)
</dt> </dl>

 

 





