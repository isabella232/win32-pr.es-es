---
description: Para mejorar la seguridad del proceso de host de proveedor compartido (wmiprvse.exe) de instrumental de administración de Windows (WMI), se realizaron cambios en las plataformas de Windows que protegen el proceso de host del proveedor con un identificador de seguridad de servicio (SID).
ms.assetid: f93ac155-512c-4efa-8168-ca2d56fe6f01
ms.tgt_platform: multiple
title: Claves y valores del Registro para controlar la seguridad del proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 916a5910a6ad21e9f9dfdcfc0992de10ae30da82
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884359"
---
# <a name="registry-keys-and-values-for-controlling-provider-security"></a>Claves y valores del Registro para controlar la seguridad del proveedor

Para mejorar la seguridad del proceso de host de proveedor compartido (wmiprvse.exe) de instrumental de administración de Windows (WMI), se realizaron cambios en las plataformas de Windows que protegen el proceso de host del proveedor con un identificador de seguridad de servicio [*(SID).*](gloss-s.md) Estos cambios presentan los siguientes modos de ejecución para el host compartido wmi: seguro y compatible.

En este tema se tratan las secciones siguientes:

-   [Modos seguros y compatibles](#secure-and-compatible-modes)
-   [Claves y valores del Registro](#registry-keys-and-values)
-   [Configurar un proveedor para que se ejecute en modo seguro o compatible](#configuring-a-provider-to-run-in-secure-or-compatible-mode)

## <a name="secure-and-compatible-modes"></a>Modos seguros y compatibles

A partir Windows 7, se agregaron los dos modos de ejecución siguientes para el proceso de host compartido wmi:

<dl> <dt>

<span id="Secure_mode"></span><span id="secure_mode"></span><span id="SECURE_MODE"></span>Modo seguro
</dt> <dd>

Los recursos de proceso de host del proveedor WMI se protegen con un [*SID de servicio.*](gloss-s.md) Solo el *SID de servicio* tiene permisos para estos recursos.

</dd> <dt>

<span id="Compatible_mode"></span><span id="compatible_mode"></span><span id="COMPATIBLE_MODE"></span>Modo compatible
</dt> <dd>

El proceso de host del proveedor compartido wmi no está protegido con un [*SID de servicio.*](gloss-s.md) El proceso de host del proveedor permite el acceso a las cuentas NetworkService o LocalService en función del modelo de hospedaje. Para obtener más información sobre los modelos de hospedaje, vea [Provider Hosting and Security](provider-hosting-and-security.md).

</dd> </dl>

**Windows Vista y Windows Server 2008:** Para acceder a las claves y valores del Registro para controlar los modos seguros y compatibles para el proceso de host del proveedor, debe instalar la actualización de seguridad en [KB 959454](https://support.microsoft.com/kb/959454). Para obtener más información, vea el Boletín [de seguridad de Microsoft MS09-012](https://www.microsoft.com/technet/security/bulletin/ms09-012.mspx).

## <a name="registry-keys-and-values"></a>Claves y valores del Registro

La configuración de modo seguro y compatible se especifica a través de claves del Registro. Las claves del Registro para WMI se encuentran en el registro en **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .

Se agregaron las siguientes claves del Registro y el valor **DWORD** que se describen en la lista siguiente para controlar el comportamiento de los proveedores WMI.

<dl> <dt>

<span id="SecuredHostProviders"></span><span id="securedhostproviders"></span><span id="SECUREDHOSTPROVIDERS"></span>**SecuredHostProviders**
</dt> <dd>

Esta clave controla el comportamiento de proveedores individuales. Todos los proveedores que aparecen en esta clave siempre se ejecutan en modo seguro. Todos los proveedores de bandeja de entrada que se incluyen Windows se enumeran en esta clave y se ejecutan en modo seguro de forma predeterminada.

Esta clave tiene prioridad sobre los proveedores enumerados en la **clave CompatibleHostProviders.**

</dd> <dt>

<span id="CompatibleHostProviders"></span><span id="compatiblehostproviders"></span><span id="COMPATIBLEHOSTPROVIDERS"></span>**CompatibleHostProviders**
</dt> <dd>

Esta clave controla el comportamiento de proveedores individuales. Todos los proveedores que aparecen en esta clave siempre se ejecutan en modo compatible. Esta clave está vacía de forma predeterminada.

Si un proveedor aparece en la clave **SecuredHostProviders** y en la clave **CompatibleHostProviders,** el proveedor se ejecuta en modo seguro.

> [!Note]  
> La **clave CompatibleHostProviders** proporciona compatibilidad de aplicaciones para aplicaciones de terceros si la clave **DefaultSecuredHost** está establecida en 1 y se sabe que el proveedor no funciona en modo seguro.

 

</dd> <dt>

<span id="DefaultSecuredHost"></span><span id="defaultsecuredhost"></span><span id="DEFAULTSECUREDHOST"></span>**DefaultSecuredHost**
</dt> <dd>

Valor **DWORD** del registro global que determina si todos los proveedores, que no aparecen en las claves **SecuredHostProviders** o **CompatibleHostProviders,** se ejecutan en modo seguro o compatible. Este **valor DWORD** permite al administrador decidir en qué modo debe ejecutarse un proveedor de terceros. De forma predeterminada, este valor se establece en cero y todos los proveedores de terceros se ejecutan en modo compatible. Los administradores pueden hacer que su equipo sea más seguro de forma predeterminada estableciendo el **valor DefaultSecuredHost** en 1.

> [!Note]  
> El **valor DefaultSecuredHost** no afecta a las demás claves del Registro. Los proveedores que aparecen en la clave **SecuredHostProviders** permanecen en modo seguro y los que aparecen en la clave **CompatibleHostProviders** permanecen en modo compatible.

 

La siguiente configuración es posible:

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Especifica que los proveedores se ejecutan en modo compatible.

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

Especifica que los proveedores se ejecutan en modo seguro.

</dd> </dl> </dd> </dl>

En la lista siguiente se enumeran los posibles valores del Registro y los modos de ejecución asociados para un proveedor.



| Se muestra en SecuredHostProviders | Aparece en CompatibleHostProviders | Configuración defaultSecuredHost | Modo       |
|-----------------------------------|--------------------------------------|----------------------------|------------|
| No                                | No                                   | 0                          | Compatible |
| No                                | Sí                                  | 0                          | Compatible |
| Sí                               | No                                   | 0                          | Seguridad     |
| Sí                               | Sí                                  | 0                          | Seguridad     |
| No                                | No                                   | 1                          | Seguridad     |
| No                                | Sí                                  | 1                          | Compatible |
| Sí                               | No                                   | 1                          | Seguridad     |
| Sí                               | Sí                                  | 1                          | Seguridad     |



 

## <a name="configuring-a-provider-to-run-in-secure-or-compatible-mode"></a>Configurar un proveedor para que se ejecute en modo seguro o compatible

Las claves del Registro se pueden modificar mediante la Consola de administración de directivas de grupo (GPMC). Para obtener más información, [vea Consola de administración de directivas de grupo](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).

Los procedimientos siguientes muestran cómo administrar la configuración de modo seguro y compatible mediante las preferencias de directiva de grupo. Para obtener más información sobre las preferencias de directiva de grupo, [vea la información general directiva de grupo preferencias de grupo.](/previous-versions/windows/it-pro/windows-server-2012-r2-and-2012/dn581922(v=ws.11))

**Para agregar un proveedor al modo seguro o compatible mediante directiva de grupo**

1.  Abra GPMC.
2.  Cree un objeto directiva de grupo (GPO).
3.  Edite el GPO.
4.  Vaya a Preferencias/Windows Configuración/Registro.
5.  Haga clic con el botón derecho y **seleccione Nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede escribir información del Registro.
6.  Seleccione el **comando** Crear.
7.  Seleccione la siguiente ruta de acceso de clave del Registro:

    **Modo seguro: HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modo compatible: HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  En el **campo** nombre, escriba el nombre del proveedor que desea agregar a esta clave. El nombre del proveedor debe tener el siguiente formato: &lt; namespace &gt; :<\_ \_ RELPATH>. Por ejemplo, root \\ cimv2: \_ \_ win32provider.name="MyProvider".
9.  En el **campo de** datos, escriba 0.
10. Haga clic en Aceptar.

**Para quitar un proveedor del modo seguro o compatible mediante directiva de grupo**

1.  Abra GPMC.
2.  Cree un GPO.
3.  Edite el GPO.
4.  Vaya a Preferencias/Windows Configuración/Registro.
5.  Haga clic con el botón derecho y **seleccione Nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede escribir información del Registro.
6.  Seleccione el **comando** Quitar.
7.  Seleccione la siguiente ruta de acceso de clave del Registro:

    **Modo seguro: HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **SecuredHostProviders**

    **Modo compatible: HKEY \_ SOFTWARE \_ DE MÁQUINA LOCAL** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **CompatibleHostProviders**

8.  En el **campo** nombre, escriba el nombre del proveedor que desea quitar de esta clave.
9.  En el **campo de** datos, escriba 0.
10. Haga clic en Aceptar.

El procedimiento siguiente proporciona detalles sobre cómo modificar el comportamiento de los proveedores que no aparecen en las claves **SecuredHostProviders** o **CompatibleHostProviders.**

**Para cambiar el valor predeterminado de la clave DefaultSecuredHost mediante directiva de grupo**

1.  Abra GPMC.
2.  Cree un GPO.
3.  Edite el GPO.
4.  Vaya a Preferencias/Windows Configuración/Registro.
5.  Haga clic con el botón derecho y **seleccione Nuevo... Registro**. Esta acción presenta una interfaz de usuario donde puede escribir información del Registro.
6.  Seleccione el **comando** Actualizar.
7.  Seleccione la siguiente ruta de acceso de clave del Registro: **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **WBEM** \\ **CIMOM**.
8.  En el **campo** nombre, escriba **DefaultSecuredHost.**
9.  En el **campo de** datos, escriba 0 para el modo compatible o 1 para el modo seguro.
10. Haga clic en Aceptar.

 

 
