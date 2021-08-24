---
description: La API de Direct3D 9 funciona en el modelo de controlador de pantalla de Windows XP (XPDM) o en el modelo de controlador de pantalla (WDDM) de Windows Vista, en función del sistema operativo instalado.
ms.assetid: b552c822-aa01-4f1d-a0a6-1411ab006e7b
title: XPDM frente a WDDM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0332198cd7c9425a3b5a107259dda1b1e974a04a2379244cdf939384260a89f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746055"
---
# <a name="xpdm-vs-wddm"></a>XPDM frente a WDDM

La API de Direct3D 9 funciona en el modelo de controlador de pantalla de Windows XP (XPDM) o en el modelo de controlador de pantalla (WDDM) de Windows Vista, en función del sistema operativo instalado. Hay algunas diferencias en la forma en que la API de Direct3D se comporta en los dos modelos de controlador.

-   [Escritorio seguro](#secure-desktop)
-   [Escritorio remoto](#remote-desktop)
-   [Servicio de Windows](#windows-service)
-   [Temas relacionados](#related-topics)

## <a name="secure-desktop"></a>Escritorio seguro

El escritorio seguro está activo siempre que se produce alguna de las siguientes situaciones: el usuario bloquea su escritorio (Windows+L), se activa el protector de pantalla (cuando no hay ningún usuario conectado) o de forma predeterminada cuando control de cuentas de usuario presenta un mensaje. Cuando el escritorio seguro está activo, no se puede acceder al dispositivo DE LAN.

Diferencias entre XPDM y WDDM:

- Se producirá un error al intentar crear un dispositivo DIRECT3D9 VBA (con **D3DERR \_ NO \_ DISPONIBLE)** y cualquier dispositivo Direct3D 9 existente indicará un código de retorno de dispositivo perdido en Present.

- Las API de Direct3D9Ex y Direct3D 10 pueden crear correctamente un dispositivo mientras el escritorio seguro está activo y las llamadas a Present [**(IDirect3D9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3d9ex) o DXGI) devolverán un código de estado que indica que el escritorio no está disponible actualmente.



 

## <a name="remote-desktop"></a>Escritorio remoto

Cuando un escritorio remoto está activo, la pantalla se controla mediante la máquina de visualización con el equipo de hospedaje que envía información a través de la red.

Diferencias entre XPDM y WDDM:

- En XPDM, se producirá un error en todos los intentos de crear un dispositivo Direct3D 9 en un escritorio remoto.

- En WDDM, el escritorio remoto admite la creación de un dispositivo DEI A través de una sesión de Escritorio remoto.



 

## <a name="windows-service"></a>Servicio de Windows

Un Windows es un proceso que se ejecuta en segundo plano, controlado por el administrador de control de servicios (SCM). Un servicio se ejecuta independientemente del escritorio activo y, por tanto, tiene una capacidad limitada para interactuar con los usuarios.

Diferencias entre XPDM y WDDM:

- En WDDM, el aislamiento de sesión 0 garantiza que un servicio no tiene acceso a ningún escritorio de usuario como medida de seguridad, por lo que un dispositivo DIRECT3D 9 nunca está disponible desde un servicio Windows.



 

> [!Note]  
> No se puede usar Direct3D 9 en un Windows servicio. Para obtener más información, consulte el [artículo de soporte técnico de Microsoft 978635](https://support.microsoft.com/kb/978635).

 


En la tabla siguiente se resumen las diferencias enumeradas aquí.



| Escritorio seguro | XPDM | WDDM (Direct3D9) | WDDM(Direct3D9Ex/Direct3D10) |
|-----------------|------|------------------|------------------------------|
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



 

Para obtener más información sobre XPDM, WDDM, Direct3D9Ex y Direct3D 10, vea API de gráficos [en Windows](../direct3darticles/graphics-apis-in-windows-vista.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
