---
description: Para mejorar la seguridad del proceso de host de proveedor compartido (wmiprvse.exe) de Instrumental de administración de Windows (WMI), se realizaron cambios en las plataformas de Windows que protegen el proceso de host de proveedor con un identificador de seguridad de servicio (SID).
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Claves y valores del registro para controlar la seguridad del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2c7dd990c1a9ebbc1242af5ce4601ce6eb22a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707275"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>Claves y valores del registro para controlar la seguridad del proveedor

Para mejorar la seguridad del proceso de host de proveedor compartido (wmiprvse.exe) de Instrumental de administración de Windows (WMI), se realizaron cambios en las plataformas de Windows que protegen el proceso de host de proveedor con un [*identificador de seguridad de servicio (SID)*](gloss-s.md). Estos cambios presentan los siguientes modos de ejecución para el host compartido WMI: seguro y compatible.

En este tema se describen las siguientes secciones:

-   [Modos seguro y compatible](#secure-and-compatible-modes)
-   [Claves y valores del registro](#registry-keys-and-values)
-   [Configuración de un proveedor para que se ejecute en modo seguro o compatible](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>Modos seguro y compatible

A partir de Windows 7, se agregaron los dos modos de ejecución siguientes para el proceso de host compartido de WMI:

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Modo seguro
</dt> <dd>

Los recursos del proceso de host del proveedor WMI están protegidos con un [*SID de servicio*](gloss-s.md). Solo el *SID del servicio* tiene permisos para estos recursos.

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Modo compatible
</dt> <dd>

El proceso de host del proveedor compartido WMI no está protegido con un [*SID de servicio*](gloss-s.md). El proceso de host del proveedor permite el acceso a las cuentas NetworkService o LocalService en función del modelo de hospedaje. Para obtener más información sobre los modelos de hospedaje, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

</dd> </dl>

**Windows Vista y Windows Server 2008:** Para tener acceso a las claves y los valores del registro para controlar los modos seguros y compatibles para el proceso de host del proveedor, debe instalar la actualización de seguridad en [KB 959454](https://support.microsoft.com/kb/959454). Para obtener más información, vea el [boletín de seguridad de Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).

## <a name="registry-keys-and-values"></a>Claves y valores del registro

La configuración de modo seguro y compatible se especifica a través de las claves del registro. Las claves del registro para WMI se encuentran en el registro en **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

Se han agregado las siguientes claves del registro y el valor **DWORD** descritos en la siguiente lista para controlar el comportamiento de los proveedores WMI.

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**
</dt> <dd>

Esta clave controla el comportamiento de los proveedores individuales. Todos los proveedores que se enumeran en esta clave siempre se ejecutan en modo seguro. Todos los proveedores de bandeja de entrada que se incluyen con Windows aparecen en esta clave y se ejecutan en modo seguro de forma predeterminada.

Esta clave tiene prioridad sobre los proveedores enumerados en la clave **CompatibleHostProviders** .

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**
</dt> <dd>

Esta clave controla el comportamiento de los proveedores individuales. Todos los proveedores que se enumeran en esta clave siempre se ejecutan en modo compatible. Esta clave está vacía de forma predeterminada.

Si un proveedor se enumera en la clave **SecuredHostProviders** y en la clave **CompatibleHostProviders** , el proveedor se ejecuta en modo seguro.

> [!Note]  
> La clave **CompatibleHostProviders** proporciona compatibilidad de aplicaciones para aplicaciones de terceros si la clave **DefaultSecuredHost** se establece en 1 y se sabe que el proveedor no funciona en modo seguro.

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

Un valor **DWORD** del registro global que determina si todos los proveedores, que no se enumeran en las claves **SecuredHostProviders** o **CompatibleHostProviders** , se ejecutan en el modo seguro o compatible. Este valor **DWORD** permite al administrador decidir en qué modo debe ejecutarse un proveedor de terceros. De forma predeterminada, este valor se establece en cero y todos los proveedores de terceros se ejecutan en modo compatible. Los administradores pueden hacer que su equipo sea más seguro de forma predeterminada si se establece el valor de **DefaultSecuredHost** en 1.

> [!Note]  
> El valor **DefaultSecuredHost** no afecta a las demás claves del registro. Los proveedores que se enumeran en la clave **SecuredHostProviders** permanecen en modo seguro y los que aparecen en la clave **CompatibleHostProviders** permanecen en modo compatible.

 

Las siguientes opciones son posibles:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Especifica que los proveedores se ejecuten en modo compatible.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Especifica que los proveedores se ejecuten en modo seguro.

</dd> </dl> </dd> </dl>

En la lista siguiente se enumeran los posibles valores del registro y los modos de ejecución asociados para un proveedor.



| Aparece en SecuredHostProviders | Aparece en CompatibleHostProviders | Configuración de DefaultSecuredHost | Mode       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| No                                | No                                   | 0                          | Compatible |
| No                                | Sí                                  | 0                          | Compatible |
| Sí                               | No                                   | 0                          | Seguridad     |
| Sí                               | Sí                                  | 0                          | Seguridad     |
| No                                | No                                   | 1                          | Seguridad     |
| No                                | Sí                                  | 1                          | Compatible |
| Sí                               | No                                   | 1                          | Seguridad     |
| Sí                               | Sí                                  | 1                          | Seguridad     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>Configuración de un proveedor para que se ejecute en modo seguro o compatible

Las claves del registro se pueden modificar mediante el Consola de administración de directivas de grupo (GPMC). Para obtener más información, vea [consola de administración de directivas de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

En los procedimientos siguientes se muestra cómo administrar la configuración de modo seguro y compatible mediante preferencias de directiva de grupo. Para obtener más información sobre las preferencias de directiva de grupo, consulte la [información general sobre las preferencias de directiva de grupo](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11)).

**Para agregar un proveedor al modo seguro o compatible mediante el uso de directiva de grupo**

1.  Abra GPMC.
2.  Cree un objeto de directiva de grupo (GPO).
3.  Edite el GPO.
4.  Vaya a preferencias/configuración de Windows/registro.
5.  Haga clic con el botón derecho y seleccione **nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.
6.  Seleccione el comando **crear** .
7.  Seleccione la siguiente ruta de acceso de clave del registro:

    **Modo seguro: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modo compatible: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  En el campo **nombre** , escriba el nombre del proveedor que desea agregar a esta clave. El nombre del proveedor debe tener el formato siguiente: <namespace> : <\_ \_ RELPATH>. Por ejemplo, la raíz \\ cimv2: \_ \_ win32provider. Name = "DataProvider".
9.  En el campo de **datos** , escriba 0.
10. Haga clic en Aceptar.

**Para quitar un proveedor del modo seguro o compatible mediante directiva de grupo**

1.  Abra GPMC.
2.  Cree un GPO.
3.  Edite el GPO.
4.  Vaya a preferencias/configuración de Windows/registro.
5.  Haga clic con el botón derecho y seleccione **nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.
6.  Seleccione el comando **quitar** .
7.  Seleccione la siguiente ruta de acceso de clave del registro:

    **Modo seguro: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modo compatible: HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  En el campo **nombre** , escriba el nombre del proveedor que desea quitar de esta clave.
9.  En el campo de **datos** , escriba 0.
10. Haga clic en Aceptar.

En el procedimiento siguiente se proporcionan detalles sobre cómo modificar el comportamiento de los proveedores que no se enumeran en las claves **SecuredHostProviders** o **CompatibleHostProviders** .

**Para cambiar el valor predeterminado de la clave DefaultSecuredHost mediante directiva de grupo**

1.  Abra GPMC.
2.  Cree un GPO.
3.  Edite el GPO.
4.  Vaya a preferencias/configuración de Windows/registro.
5.  Haga clic con el botón derecho y seleccione **nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede especificar la información del registro.
6.  Seleccione el comando de **actualización** .
7.  Seleccione la siguiente ruta de acceso de clave del registro: **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.
8.  En el campo **nombre** , escriba **DefaultSecuredHost**.
9.  En el campo de **datos** , escriba 0 para el modo compatible o 1 para el modo seguro.
10. Haga clic en Aceptar.

 

 
