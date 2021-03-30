---
title: Interfaz IVMGuestOS (VPCCOMInterfaces. h)
description: Define el sistema operativo invitado que se ejecuta en una máquina virtual.
ms.assetid: fb31f294-94ad-4545-8d59-849a5f2fe780
keywords:
- Interfaz IVMGuestOS Virtual PC
- Interfaz IVMGuestOS Virtual PC, descripción
topic_type:
- apiref
api_name:
- IVMGuestOS
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b52d4f7651a21b1baad31448e47866dfb5bf4c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150997"
---
# <a name="ivmguestos-interface"></a>Interfaz IVMGuestOS

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define el sistema operativo invitado que se ejecuta en una máquina virtual. Esta interfaz permite interactuar con los componentes de integración que se ejecutan en el sistema operativo invitado. El **IVMGuestOS** de una máquina virtual se puede recuperar mediante la propiedad [**IVMVirtualMachine:: Guests**](ivmvirtualmachine-guestos.md) .

## <a name="members"></a>Miembros

La interfaz **IVMGuestOS** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMGuestOS** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IVMGuestOS** tiene estos métodos.



| Método                                                                          | Descripción                                                                                             |
|:--------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetOsVersionInfo**](ivmguestos-getosversioninfo.md)                         | Recupera información de versión del sistema operativo invitado que se ejecuta en la máquina virtual.<br/> |
| [**GetParameter**](ivmguestos-getparameter.md)                                 | Recupera un parámetro con nombre en el invitado.<br/>                                                |
| [**InstallIntegrationComponents**](ivmguestos-installintegrationcomponents.md) | Busca e instala los componentes de integración más recientes en el sistema operativo invitado.<br/>      |
| [**IsUserLoggedOn**](ivmguestos-isuserloggedon.md)                             | Determina si la sesión solicitada está presente.<br/>                                         |
| [**Forzado**](ivmguestos-logoff.md)                                             | Cierra la sesión de todos los usuarios del sistema operativo invitado.<br/>                                          |
| [**Volver**](ivmguestos-restart.md)                                           | Reinicia el sistema operativo invitado.<br/>                                                         |
| [**SetParameter**](ivmguestos-setparameter.md)                                 | Establece un parámetro con nombre en el invitado.<br/>                                                     |
| [**Apagado**](ivmguestos-shutdown.md)                                         | Apaga el sistema operativo invitado.<br/>                                                       |



 

### <a name="properties"></a>Propiedades

La interfaz **IVMGuestOS** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                                                                                                                 |
|:-------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanShutdown**](ivmguestos-canshutdown.md)<br/>                                   | Solo lectura<br/>  | Indica si el sistema operativo invitado se puede apagar sin problemas (requiere componentes de integración).<br/>                         |
| [**ComputerName**](ivmguestos-computername.md)<br/>                                 | Solo lectura<br/>  | El nombre de equipo del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                  |
| [**CSDVersion**](ivmguestos-csdversion.md)<br/>                                     | Solo lectura<br/>  | El CSDVersion del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                     |
| [**HeartbeatPercentage**](ivmguestos-heartbeatpercentage.md)<br/>                   | Solo lectura<br/>  | Porcentaje de latidos esperados recibidos en el último minuto.<br/>                                                             |
| [**IntegrationComponentsVersion**](ivmguestos-integrationcomponentsversion.md)<br/> | Solo lectura<br/>  | La versión de los componentes de integración de instalados en el sistema operativo invitado.<br/>                                               |
| [**IsHeartbeating**](ivmguestos-isheartbeating.md)<br/>                             | Solo lectura<br/>  | Indica si la máquina virtual tiene un latido.<br/>                                                                           |
| [**IsHostTimeSyncEnabled**](ivmguestos-ishosttimesyncenabled.md)<br/>               | Lectura/escritura<br/> | Indica si los componentes de integración de esta máquina virtual deben sincronizar el reloj del invitado con el reloj del host.<br/> |
| [**MultipleUserSessionsAllowed**](ivmguestos-multipleusersessionsallowed.md)<br/>   | Solo lectura<br/>  | Indica si se permiten varias sesiones de usuario simultáneas en el sistema operativo invitado.<br/>                                 |
| [**OSBuildNumber**](ivmguestos-osbuildnumber.md)<br/>                               | Solo lectura<br/>  | El número de compilación del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                   |
| [**OSMajorVersion**](ivmguestos-osmajorversion.md)<br/>                             | Solo lectura<br/>  | La versión principal del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                  |
| [**OSMinorVersion**](ivmguestos-osminorversion.md)<br/>                             | Solo lectura<br/>  | La versión secundaria del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                  |
| [**OSName**](ivmguestos-osname.md)<br/>                                             | Solo lectura<br/>  | Nombre del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                           |
| [**OSPlatformId**](ivmguestos-osplatformid.md)<br/>                                 | Solo lectura<br/>  | El identificador de plataforma del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                            |
| [**OSVersion**](ivmguestos-osversion.md)<br/>                                       | Solo lectura<br/>  | La versión del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                        |
| [**ProductType**](ivmguestos-producttype.md)<br/>                                   | Solo lectura<br/>  | El tipo de producto del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                   |
| [**ScreenLocked**](ivmguestos-screenlocked.md)<br/>                                 | Solo lectura<br/>  | Indica si la pantalla está bloqueada en el sistema operativo invitado.<br/>                                                            |
| [**ServicePackMajor**](ivmguestos-servicepackmajor.md)<br/>                         | Solo lectura<br/>  | La versión principal del Service Pack del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                              |
| [**ServicePackMinor**](ivmguestos-servicepackminor.md)<br/>                         | Solo lectura<br/>  | Versión secundaria del Service Pack del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                              |
| [**SuiteMask**](ivmguestos-suitemask.md)<br/>                                       | Solo lectura<br/>  | El SuiteMask del sistema operativo invitado que se ejecuta en la máquina virtual.<br/>                                                      |
| [**TerminalServerPort**](ivmguestos-terminalserverport.md)<br/>                     | Solo lectura<br/>  | Puerto usado por Servicios de Escritorio remoto en el sistema operativo invitado.<br/>                                                              |
| [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md)<br/>   | Solo lectura<br/>  | El estado de la inicialización de Terminal Services en el sistema operativo invitado.<br/>                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be<br/>                 |



 

