---
description: Los proveedores WMI también pueden mantener registros. Los archivos de registro que aparecen en un sistema dependen de los proveedores instalados.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: Archivos de registro del proveedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0b485c16c44ad5ac26c51db7551baa423ad1a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908543"
---
# <a name="wmi-provider-log-files"></a>Archivos de registro del proveedor WMI

Los proveedores WMI también pueden mantener registros. Los archivos de registro que aparecen en un sistema dependen de los proveedores instalados.

Estos registros pueden encontrarse en el directorio% SystemRoot% \\ system32 \\ WBEM \\ logs.

-   [Wmiprov. log](#wmiprovlog)
-   [Ntevt. log](#ntevtlog)
-   [Dsprovider. log](#dsproviderlog)
-   [Temas relacionados](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov. log

El archivo Wmiprov. log contiene los datos y los eventos de administración de los controladores de Modelo de controlador de Windows (WDM) habilitados para WMI y el [proveedor de WDM](/windows/desktop/WmiCoreProv/wdm-provider). Proporciona información sobre advertencias y errores principalmente para la solución de problemas y la depuración de las aplicaciones cliente y de proveedor que la usan.

Wmiprov. log contiene:

-   Errores del [proveedor de WDM](/windows/desktop/WmiCoreProv/wdm-provider) o del controlador de dispositivo, como la compilación de MOF binarios con errores o errores al recuperar datos.
-   El estado de la compilación de MOF para cada uno de los controladores que usan el formato MOF.
-   Eventos de construcción y desconstrucción de proveedores.
-   Copia impresa de WNODE.

## <a name="ntevtlog"></a>Ntevt. log

El archivo Ntevt. log contiene los mensajes de seguimiento del [proveedor de registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider. log

El archivo Dsprovider. log contiene información de seguimiento y mensajes de error para el [proveedor de Active Directory](/previous-versions/windows/desktop/dsprov/active-directory-provider).

En la tabla siguiente se enumeran algunos problemas comunes que pueden producirse y se ofrecen posibles causas y soluciones.



| Message                                                                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR de CLDAPClassProvider:: InitializeLDAPProvider ADsGetObject en RootDSE: <hresult>                                                                                                                                                                                                                    | Error en la llamada ADSI al intentar obtener la raíz de los servicios de directorio. Compruebe que el equipo es miembro de un dominio.                                                                                                                                                                                                                                                                             |
| ERROR de CDSClassProvider:: GetObjectAsync () GetClassFromCacheOrADSI para <class name> con <hresult>                                                                                                                                                                                                  | La clase que está intentando obtener no es una clase válida en el directorio. Compruebe que el nombre de la clase es correcto.                                                                                                                                                                                                                                                                                                |
| ERROR de CLDAPInstanceProvider::P utInstanceAsync () ModifyExistingInstance para LDAP: el protocolo de error de foo1, CN = users, DC = dsprovider, DC = nttest, DC = Microsoft, DC = com con <hresult>                                                                                                                                       | El proveedor no pudo escribir una instancia modificada en los servicios de directorio. Asegúrese de que está usando la interfaz [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para especificar el conjunto de propiedades que va a modificar. Para obtener más información sobre cómo usar la interfaz **IWbemContext** con [**PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long)), vea [actualizar una instancia completa](updating-an-entire-instance.md). |
| ERROR de CLDAPHelper:: GetADSIInstance ADsOpenObject () en <class name> con <hresult><br/> ERROR de CLDAPInstanceProvider:: GetObjectAsync: GetADSIInstance () con <hresult><br/> ERROR de CLDAPInstanceProvider:: GetObjectAsync () para el usuario de DS \_ . ADSIPath = "<class name><br/> | Estos tres mensajes indican que la instancia que está intentando obtener no existe en el servicio de directorio. Compruebe que el valor de **ADSIPath** y el nombre de clase son correctos.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos de registro de WMI](wmi-log-files.md)
</dt> </dl>

 

