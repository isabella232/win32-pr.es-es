---
description: Los proveedores WMI también pueden mantener registros. Los archivos de registro que aparecen en un sistema dependen de qué proveedores estén instalados.
ms.assetid: 04f041e5-4f2c-4c94-9aba-b040d941b46d
ms.tgt_platform: multiple
title: Archivos de registro del proveedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed9cc74b9f1c6be16f1d85eb1e1863e0dc8b7b33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889161"
---
# <a name="wmi-provider-log-files"></a>Archivos de registro del proveedor WMI

Los proveedores WMI también pueden mantener registros. Los archivos de registro que aparecen en un sistema dependen de qué proveedores estén instalados.

Estos registros pueden encontrarse en el directorio %systemroot% \\ system32 \\ wbem \\ logs.

-   [Wmiprov.log](#wmiprovlog)
-   [Ntevt.log](#ntevtlog)
-   [Dsprovider.log](#dsproviderlog)
-   [Temas relacionados](#related-topics)

## <a name="wmiprovlog"></a>Wmiprov.log

El archivo Wmiprov.log contiene datos de administración y eventos de controladores de modelo de controlador de Windows habilitados para WMI (WDM) y el [proveedor WDM](/windows/desktop/WmiCoreProv/wdm-provider). Proporciona información de advertencia y error principalmente para solucionar problemas y depurar el proveedor y las aplicaciones cliente que la usan.

Wmiprov.log contiene:

-   Errores del proveedor [de WDM](/windows/desktop/WmiCoreProv/wdm-provider) o del controlador de dispositivo, como el error de compilación binaria de MOF o el error al recuperar datos.
-   El estado de la compilación de MOF para cada uno de los controladores que usan el formato MOF.
-   Eventos de construcción y deconstrucción del proveedor.
-   Impresión de WNODE.

## <a name="ntevtlog"></a>Ntevt.log

El archivo Ntevt.log contiene mensajes de seguimiento del proveedor [de registro de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider).

## <a name="dsproviderlog"></a>Dsprovider.log

El archivo Dsprovider.log contiene información de seguimiento y mensajes de error [para Active Directory provider](/previous-versions/windows/desktop/dsprov/active-directory-provider).

En la tabla siguiente se enumeran algunos problemas comunes que pueden producirse y se ofrecen posibles causas y soluciones.



| Message                                                                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CLDAPClassProvider::InitializeLDAPProvider ADsGetObject on RootDSE FAILED : &lt; hresult&gt;                                                                                                                                                                                                                    | Error en la llamada ADSI al intentar obtener la raíz de los servicios de directorio. Compruebe que el equipo es miembro de un dominio.                                                                                                                                                                                                                                                                             |
| CDSClassProvider::GetObjectAsync() GetClassFromCacheOrADSI FAILED for <class name> with &lt; hresult&gt;                                                                                                                                                                                                  | La clase que está intentando obtener no es una clase válida en el directorio . Compruebe que el nombre de clase es correcto.                                                                                                                                                                                                                                                                                                |
| CLDAPInstanceProvider::P utInstanceAsync() ModifyExistingInstance FAILED for LDAP://CN=foo1, CN=Users, DC=dsprovider,DC=nttest, DC=Microsoft, DC=com with &lt; hresult&gt;                                                                                                                                       | El proveedor no pudo escribir una instancia modificada en los servicios de directorio. Asegúrese de que usa la [**interfaz IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para especificar el conjunto de propiedades que va a modificar. Para obtener más información sobre cómo usar la **interfaz IWbemContext** [**con PutInstance**](/windows/desktop/api/Provider/nf-provider-provider-putinstance(constcinstance__long)), vea [Actualización de una instancia completa](updating-an-entire-instance.md)de . |
| CLDAPHelper::GetADSIInstance ADsOpenObject() FAILED on <class name> with &lt; hresult&gt;<br/> CLDAPInstanceProvider::GetObjectAsync : GetADSIInstance() FAILED with &lt; hresult&gt;<br/> CLDAPInstanceProvider::GetObjectAsync() FAILED for ds \_ user. ADSIPath="<class name><br/> | Estos tres mensajes indican que la instancia que está intentando obtener no existe en el servicio de directorio. Compruebe que el **valor ADSIPath** y el nombre de clase son correctos.                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos de registro WMI](wmi-log-files.md)
</dt> </dl>

 

