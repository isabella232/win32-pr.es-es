---
description: La API de Direct3D 9 funciona en el modelo de controladores de pantalla de Windows XP (XPDM) o en el modelo de controladores de pantalla (WDDM) de Windows Vista, dependiendo del sistema operativo instalado.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM frente a WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccdf4bba28b53959d8e86d8928c786db3b1d0c7f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686284"
---
# <a name="xpdm-vs-wddm"></a>XPDM frente a WDDM

La API de Direct3D 9 funciona en el modelo de controladores de pantalla de Windows XP (XPDM) o en el modelo de controladores de pantalla (WDDM) de Windows Vista, dependiendo del sistema operativo instalado. Hay algunas diferencias en la forma en que la API de Direct3D se comporta en los dos modelos de controladores.

-   [Escritorio seguro](#secure-desktop)
-   [Escritorio remoto](#remote-desktop)
-   [Servicio de Windows](#windows-service)
-   [Temas relacionados](#related-topics)

## <a name="secure-desktop"></a>Escritorio seguro

El escritorio seguro está activo siempre que se produzca cualquiera de las siguientes situaciones: el usuario bloquea el escritorio (Windows + L), se activa el protector de pantalla (cuando ningún usuario ha iniciado sesión) o de forma predeterminada cuando el control de cuentas de usuario presenta un mensaje. Cuando el escritorio seguro está activo, el dispositivo HAL no es accesible.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre XPDM y WDDM:<br/> Se producirá un error al intentar crear un dispositivo HAL de Direct3D9 (con **D3DERR \_ no \_ disponible**) y cualquier dispositivo de Direct3D 9 existente indicará un código de retorno de dispositivo perdido en este momento.<br/> Las API de Direct3D9Ex y Direct3D 10 pueden crear correctamente un dispositivo mientras el escritorio seguro está activo y las llamadas a Present ([**IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) devolverán un código de estado que indica que el escritorio no está disponible actualmente.<br/> |



 

## <a name="remote-desktop"></a>Escritorio remoto

Cuando un escritorio remoto está activo, la pantalla se encarga de la visualización con el equipo host enviando información a través de la red.



|                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre XPDM y WDDM:<br/> En XPDM, se producirá un error en todos los intentos de crear un dispositivo de Direct3D 9 en un escritorio remoto.<br/> En WDDM, escritorio remoto admite la creación de un dispositivo HAL a través de una sesión de escritorio remoto.<br/> |



 

## <a name="windows-service"></a>Servicio de Windows

Un servicio de Windows es un proceso que se ejecuta en segundo plano, controlado por el administrador de control de servicios (SCM). Un servicio se ejecuta de forma independiente del escritorio activo y, por tanto, tiene una capacidad limitada para interactuar con los usuarios.



|                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferencias entre XPDM y WDDM:<br/> En WDDM, el aislamiento de sesión 0 garantiza que un servicio no tiene acceso a ningún escritorio de usuario como medida de seguridad; por lo tanto, un dispositivo HAL de Direct3D 9 nunca está disponible desde un servicio de Windows.<br/> |



 

> [!Note]  
> No se puede usar Direct3D 9 en un servicio de Windows. Para obtener más información, vea el [artículo de soporte técnico de Microsoft 978635](https://support.microsoft.com/kb/978635).

 


En la tabla siguiente se resumen las diferencias que se muestran aquí.



|                 | XPDM | WDDM (Direct3D9) | WDDM (Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
| Escritorio seguro  |      |                  |                              |
| NULLREF         | Sí  | Sí              | Sí                          |
| HAL             | No   | No               | Sí                          |
| REF             | Sí  | Sí              | Sí                          |
| Escritorio remoto  |      |                  |                              |
| NULLREF         | No   | Sí              | Sí                          |
| HAL             | No   | Sí              | Sí                          |
| REF             | Sí  | Sí              | Sí                          |
| Servicio de Windows |      |                  |                              |
| NULLREF         | No   | No               | No                           |
| HAL             | No   | No               | No                           |
| REF             | No   | No               | No                           |
| WARP10          | N/D  | N/D              | Sí                          |



 

Para obtener más información sobre XPDM, WDDM, Direct3D9Ex y Direct3D 10, vea [API de gráficos en Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
