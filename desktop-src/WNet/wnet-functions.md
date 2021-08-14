---
title: Funciones de WNet
description: Windows Las funciones de red proporcionan información y utilidades para administrar recursos de red.
ms.assetid: 8a83186f-a912-4c61-8137-1f6be1f3afd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771974bcc2967ddba32439bb655173f62b8478ad367e086e620ca02825a2567f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330790"
---
# <a name="wnet-functions"></a>Funciones de WNet

Windows Las funciones de red proporcionan información y utilidades para administrar recursos de red. Las Windows de red se pueden agrupar de la siguiente manera:

-   [Funciones de conexión](#connection-functions)
-   [Funciones de enumeración](#enumeration-functions)
-   [Funciones de información](#information-functions)
-   [Funciones de usuario](#user-functions)

## <a name="connection-functions"></a>Funciones de conexión

Llame a las siguientes funciones de conexión de WNet para conectar un dispositivo local a un recurso de red y cancelar las conexiones de red.



| Función                                                                     | Descripción                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MultinetGetConnectionPerformance**](/windows/win32/api/winnetwk/nf-winnetwk-multinetgetconnectionperformancea) | Devuelve información sobre el rendimiento esperado de una conexión a un recurso de red.                                                                                                                                      |
| [**WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona)                               | Conecta un dispositivo local a un recurso de red. (Se proporciona por compatibilidad con versiones de 16 bits de Windows).                                                                                                                   |
| [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a)                             | Conecta un dispositivo local a un recurso de red.                                                                                                                                                                                 |
| [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)                             | Conecta un dispositivo local a un recurso de red. Esta función incluye un parámetro más que la función **WNetAddConnection2,** un identificador de una ventana que el proveedor de red puede usar como ventana de propietario para los cuadros de diálogo. |
| [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona)                         | Cancela una conexión de red. (Se proporciona por compatibilidad con versiones de 16 bits de Windows).                                                                                                                                    |
| [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a)                       | Cancela una conexión de red, lo que proporciona la capacidad de actualizar el perfil de usuario con información sobre las conexiones persistentes.                                                                                                  |
| [**WNetConnectionDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog)                         | Inicia un cuadro de diálogo de exploración general para conectarse a los recursos de red.                                                                                                                                                      |
| [**WNetConnectionDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetconnectiondialog1a)                       | Inicia un cuadro de diálogo de exploración general para conectarse a recursos de red mediante una [**estructura CONNECTDLGSTRUCT.**](/windows/win32/api/winnetwk/ns-winnetwk-connectdlgstructa)                                                                                  |
| [**WNetDisconnectDialog**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog)                         | Inicia un cuadro de diálogo de exploración general para desconectarse de los recursos de red.                                                                                                                                                 |
| [**WNetDisconnectDialog1**](/windows/win32/api/winnetwk/nf-winnetwk-wnetdisconnectdialog1a)                       | Inicia un cuadro de diálogo de exploración general para desconectarse de los recursos de red, mediante una [**estructura DISCDLGSTRUCT.**](/windows/win32/api/winnetwk/ns-winnetwk-discdlgstructa)                                                                                   |
| [**WNetGetConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetconnectiona)                               | Recupera el nombre del recurso de red asociado a un dispositivo local.                                                                                                                                                     |
| [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea)                         | Cuando se le asigna una ruta de acceso basada en unidad para un recurso de red, devuelve una forma más universal del nombre.                                                                                                                               |
| [**WNetRestoreConnectionW**](/windows/win32/api/winnetwk/nf-winnetwk-wnetrestoreconnectionw)                     | Restaura la conexión a un recurso de red, solicitando al usuario, si es necesario, un nombre y una contraseña.                                                                                                                      |
| [**WNetUseConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetuseconnectiona)                               | Conecta un dispositivo local a un recurso de red; selecciona automáticamente un dispositivo local sin usar para redirigir al recurso de red.                                                                                               |



 

> [!Note]  
> Las [**funciones WNetAddConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnectiona) y [**WNetCancelConnection**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnectiona) se admiten para la compatibilidad con Windows para grupos de trabajo. Sin embargo, las nuevas aplicaciones deben usar [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) o [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a)y [**WNetCancelConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcancelconnection2a).

 

## <a name="enumeration-functions"></a>Funciones de enumeración

Llame a las siguientes funciones de WNet para enumerar los recursos de red.



| Función                                     | Descripción                                                                             |
|----------------------------------------------|-----------------------------------------------------------------------------------------|
| [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum)       | Finaliza una enumeración de recursos de red.                                                    |
| [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) | Continúa una enumeración de recursos de red iniciados por **la función WNetOpenEnum.** |
| [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)         | Inicia una enumeración de recursos de red.                                             |



 

## <a name="information-functions"></a>Funciones de información

Llame a las siguientes funciones de utilidad e información de WNet para recuperar el proveedor de red y otra información.



| Función                                                         | Descripción                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WNetGetLastError**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetlasterrora)                     | Devuelve el código de error más reciente establecido por una función de WNet, el que notifica un proveedor de red.  |
| [**WNetGetNetworkInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetnetworkinformationa)   | Devuelve información extendida sobre un proveedor de red específico.                                     |
| [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)               | Devuelve el nombre del proveedor para un tipo específico de red.                                           |
| [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) | Devuelve el proveedor de red que posee un recurso y obtiene información sobre el tipo de recurso. |
| [**WNetGetResourceParent**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceparenta)           | Devuelve el elemento primario de un recurso de red.                                                           |



 

## <a name="user-functions"></a>Funciones de usuario

Llame a la siguiente función de WNet para recuperar el nombre del usuario asociado a un dispositivo local.



| Función                           | Descripción                                                                              |
|------------------------------------|------------------------------------------------------------------------------------------|
| [**WNetGetUser**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetusera) | Devuelve el nombre de usuario predeterminado actual o el nombre de usuario que estableció la conexión. |



 

Muchas de las funciones de WNet usan una [**estructura NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) para almacenar información sobre un recurso de red.

 

 