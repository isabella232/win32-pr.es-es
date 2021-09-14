---
description: El método AdvertiseProduct del objeto Installer anuncia un paquete de instalación.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: Installer::AdvertiseProduct (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171753"
---
# <a name="installeradvertiseproduct-method"></a>Installer::AdvertiseProduct (método)

El **método AdvertiseProduct** del [**objeto Installer**](installer-object.md) anuncia un paquete de instalación.

## <a name="syntax"></a>Sintaxis


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*packagePath* 
</dt> <dd>

Ruta de acceso completa al paquete Windows instalador (.msi) que se va a anunciar.

</dd> <dt>

*contextoo* 
</dt> <dd>

Contexto del anuncio. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt> </dl> | Anuncia la aplicación para una instalación en el contexto de instalación [por máquina](installation-context.md). Esto hace que todos los usuarios del equipo puedan instalar el paquete.<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**msiAdvertiseProductUser**</dt> <dt>1</dt> </dl>             | Anuncia la aplicación para una instalación en el contexto de instalación [por usuario](installation-context.md).<br/>                                                                                   |



 

</dd> <dt>

*Transforma* 
</dt> <dd>

Lista de transformaciones que se aplicarán al producto. Las transformaciones de la lista se delimitan mediante punto y coma. Este parámetro es opcional.

</dd> <dt>

*language* 
</dt> <dd>

Idioma del paquete de instalación que se usará. Este parámetro es opcional.

</dd> <dt>

*options* 
</dt> <dd>

Opciones de anuncio. Este parámetro es opcional. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Anuncio estándar<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Anuncia una nueva instancia del producto. Requiere que la primera transformación de la lista de transformaciones del parámetro *transforms* sea la transformación de instancia que cambia el código del producto. Para obtener más información, [vea Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **método AdvertiseProduct** usa la [**función MsiAdvertiseProductEx.**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso del **método AdvertiseProduct.**


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




