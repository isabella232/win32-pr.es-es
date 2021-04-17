---
description: La propiedad InstallProperty es el valor de la propiedad para la instancia de este producto. Esta propiedad llama a la función MsiGetProductInfoEx, con el ProductCode, UserSid y el contexto del objeto Product y la propiedad solicitada como un parámetro.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Product. InstallProperty (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.InstallProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12949997363fce8073c15f7ca6b7312c211fa0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653425"
---
# <a name="productinstallproperty-method"></a>Product. InstallProperty (método)

La propiedad **InstallProperty** es el valor de la propiedad para la instancia de este producto.

Esta propiedad llama a la función [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) , con el *ProductCode*, *UserSid* y el *contexto* del objeto [**Product**](product-object.md) y la propiedad solicitada como un parámetro.

## <a name="syntax"></a>Sintaxis


```JScript
Product.InstallProperty(
  property
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*property* 
</dt> <dd>

Especifica la propiedad que se va a recuperar. Las propiedades de la lista siguiente solo se pueden recuperar de aplicaciones que ya están instaladas. Tenga en cuenta que se garantiza que las propiedades [necesarias](required-properties.md) están disponibles, pero otras propiedades solo están disponibles si se ha establecido esa propiedad. Vea los vínculos indicados a las [propiedades](properties.md) del instalador para obtener información sobre cómo se establece cada propiedad.



| Propiedades instaladas                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**INSTALLPROPERTY \_ PRODUCTSTATE**</dt> </dl>                         | Estado del producto devuelto en forma de cadena como "1" para el anunciad y "5" para instalado.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALLPROPERTY \_ HELPLINK**</dt> </dl>                                     | Vínculo de soporte técnico. Para obtener más información, vea la propiedad [**ARPHELPLINK**](arphelplink.md) .<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**INSTALLPROPERTY \_ HELPTELEPHONE**</dt> </dl>                      | Teléfono de soporte técnico. Para obtener más información, vea la propiedad [**ARPHELPTELEPHONE**](arphelptelephone.md) .<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLDATE**</dt> </dl>                            | La última vez que este producto recibió el servicio. El valor de esta propiedad se reemplaza cada vez que se aplica o quita una revisión del producto o se usa la [opción de línea de comandos](command-line-options.md) /v para reparar el producto. Si el producto no ha recibido ninguna reparación o revisión, esta propiedad contiene la hora en que se instaló este producto en este equipo.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLEDPRODUCTNAME**</dt> </dl> | Nombre del producto instalado. Para obtener más información, vea la propiedad [**ProductName**](productname.md) .<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALLPROPERTY \_ installLocation**</dt> </dl>                | Ubicación de instalación. Para obtener más información, vea la propiedad [**ARPINSTALLLOCATION**](arpinstalllocation.md) .<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLSOURCE**</dt> </dl>                      | Origen de la instalación. Para obtener más información, vea la propiedad [**SourceDir**](sourcedir.md) .<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**INSTALLPROPERTY \_ LOCALPACKAGE**</dt> </dl>                         | Paquete local almacenado en caché.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**\_publicador de INSTALLPROPERTY**</dt> </dl>                                  | Editor. Para obtener más información, vea la propiedad [**manufacturer**](manufacturer.md) .<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**INSTALLPROPERTY \_ URLINFOABOUT**</dt> </dl>                         | Información de la dirección URL. Para obtener más información, vea la propiedad [**ARPURLINFOABOUT**](arpurlinfoabout.md) .<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**INSTALLPROPERTY \_ URLUPDATEINFO**</dt> </dl>                      | Información de actualización de URL. Para obtener más información, vea la propiedad [**ARPURLUPDATEINFO**](arpurlupdateinfo.md) .<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMINOR**</dt> </dl>                         | Versión secundaria del producto derivada de la propiedad [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**INSTALLPROPERTY \_ propiedad versionmajor**</dt> </dl>                         | Versión principal del producto derivada de la propiedad [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONSTRING**</dt> </dl>                      | Versión del producto. Para obtener más información, vea la propiedad [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                    |



 

Para recuperar el identificador de producto, el propietario registrado o la compañía registrada de las aplicaciones que ya están instaladas, establezca la *propiedad* en uno de los siguientes valores de cadena de texto.



| Value      | Descripción                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | Identificador del producto. Para obtener más información, vea la propiedad [**ProductID**](productid.md) . |
| RegCompany | La compañía registrada para usar este producto.                                                    |
| RegOwner   | Propietario registrado para usar este producto.                                                      |



 

Para recuperar el tipo de instancia del producto, establezca la *propiedad* en el valor siguiente. Esta propiedad está disponible para los productos anunciados o instalados.



| Value        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | Un valor que falta o un valor de 0 indica una instalación de producto normal. Un valor de 1 indica un producto instalado mediante una transformación de varias instancias y la propiedad [**MSINEWINSTANCE**](msinewinstance.md) . Está disponible con el instalador que ejecuta Windows Server 2003 o Windows XP con SP1. Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md). |



 

También se pueden recuperar las propiedades de la siguiente lista de las aplicaciones que se anuncian. Estas propiedades no se pueden recuperar para las instancias de producto que se instalan en un contexto por usuario no administrado para cuentas de usuario distintas de la cuenta de usuario actual.



| Propiedades anunciadas                 | Descripción                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transformaciones de INSTALLPROPERTY \_           | Transformaciones.                                                                                                                                                                                                                                                                                          |
| \_lenguaje INSTALLPROPERTY             | Idioma del producto.                                                                                                                                                                                                                                                                                    |
| INSTALLPROPERTY \_ NombreProducto          | Legible: nombre del producto. Para obtener más información, vea la propiedad [**ProductName**](productname.md) .                                                                                                                                                                                              |
| INSTALLPROPERTY \_ ASSIGNMENTTYPE       | Es igual a cero (0) si el producto se anuncia o se instala por usuario. Es igual a uno (1) si el producto se anuncia o se instala por equipo para todos los usuarios.<br/>                                                                                                                                  |
| INSTALLPROPERTY \_ PACKAGECODE          | Identificador del paquete desde el que se instaló este producto. Para obtener más información, consulte [códigos de paquete](package-codes.md).                                                                                                                                                                                      |
| versión de INSTALLPROPERTY \_              | Versión del producto derivada de la propiedad [**ProductVersion**](productversion.md) .                                                                                                                                                                                                                  |
| INSTALLPROPERTY \_ PRODUCTICON          | Icono principal del paquete. Para obtener más información, vea la propiedad [**ARPPRODUCTICON**](arpproducticon.md) .                                                                                                                                                                                       |
| INSTALLPROPERTY \_ PACKAGENAME          | Nombre del paquete de instalación original.                                                                                                                                                                                                                                                           |
| \_aplicación Lua autorizada de INSTALLPROPERTY \_ \_ | Un valor de 1 indica un producto al que pueden atender los usuarios que no son administradores mediante la [revisión del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md). Un valor que falta o un valor de 0 indica que la revisión con privilegios mínimos no está habilitada. Disponible con Windows Installer 3,0 y versiones posteriores. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la llamada se realiza correctamente, la propiedad contiene el valor como una cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Manuales**](product-object.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




