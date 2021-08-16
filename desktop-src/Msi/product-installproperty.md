---
description: La propiedad InstallProperty es el valor de la propiedad para la instancia de este producto. Esta propiedad llama a la función MsiGetProductInfoEx, con los valores ProductCode, UserSid y Context del objeto Product y la propiedad solicitada como parámetro.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Método Product.InstallProperty
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
ms.openlocfilehash: 3beb67ccdd4a50cdbb52e41846f46fcb4f2545dd833d30098e29c4d5887f8fae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926075"
---
# <a name="productinstallproperty-method"></a>Método Product.InstallProperty

La **propiedad InstallProperty** es el valor de la propiedad para la instancia de este producto.

Esta propiedad llama a [**la función MsiGetProductInfoEx,**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) con los valores *ProductCode*, *UserSid* y *Context* del objeto [**Product**](product-object.md) y la propiedad solicitada como parámetro.

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

Especifica la propiedad que se va a recuperar. Las propiedades de la lista siguiente solo se pueden recuperar de las aplicaciones que ya están instaladas. Tenga en [cuenta que](required-properties.md) se garantiza que las propiedades necesarias estén disponibles, pero otras solo están disponibles si se ha establecido esa propiedad. Consulte los vínculos indicados a las propiedades del [instalador](properties.md) para obtener información sobre cómo se establece cada propiedad.



| Propiedades instaladas                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**INSTALLPROPERTY \_ PRODUCTSTATE**</dt> </dl>                         | Estado del producto devuelto en forma de cadena como "1" para Anunciado y "5" para instalado.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALLPROPERTY \_ HELPLINK**</dt> </dl>                                     | Vínculo de soporte técnico. Para obtener más información, vea la [**propiedad ARPHELPLINK.**](arphelplink.md)<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**INSTALLPROPERTY \_ HELPTELEPHONE**</dt> </dl>                      | Teléfono de soporte técnico. Para obtener más información, vea la [**propiedad ARPHELPTELEPHONE.**](arphelptelephone.md)<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLDATE**</dt> </dl>                            | La última vez que este producto recibió el servicio. El valor de esta propiedad se reemplaza cada vez que se aplica o quita una revisión del producto o se usa la opción de línea de comandos [/v](command-line-options.md) para reparar el producto. Si el producto no ha recibido ninguna reparación o revisión, esta propiedad contiene la hora en que se instaló este producto en este equipo.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLEDPRODUCTNAME**</dt> </dl> | Nombre del producto instalado. Para obtener más información, vea la [**propiedad ProductName.**](productname.md)<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLLOCATION**</dt> </dl>                | Ubicación de instalación. Para obtener más información, vea la [**propiedad ARPINSTALLLOCATION.**](arpinstalllocation.md)<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLSOURCE**</dt> </dl>                      | Origen de instalación. Para obtener más información, vea la [**propiedad SourceDir.**](sourcedir.md)<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**INSTALLPROPERTY \_ LOCALPACKAGE**</dt> </dl>                         | Paquete almacenado en caché local.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**INSTALLPROPERTY \_ PUBLISHER**</dt> </dl>                                  | Editor. Para obtener más información, vea la [**propiedad**](manufacturer.md) Fabricante.<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**INSTALLPROPERTY \_ URLINFOABOUT**</dt> </dl>                         | Información de dirección URL. Para obtener más información, vea la [**propiedad ARPURLINFOABOUT.**](arpurlinfoabout.md)<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**INSTALLPROPERTY \_ URLUPDATEINFO**</dt> </dl>                      | Información de actualización de direcciones URL. Para obtener más información, vea la [**propiedad ARPURLUPDATEINFO.**](arpurlupdateinfo.md)<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMINOR**</dt> </dl>                         | Versión secundaria del producto derivada de la [**propiedad ProductVersion.**](productversion.md)<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMAJOR**</dt> </dl>                         | Versión principal del producto derivada de la [**propiedad ProductVersion.**](productversion.md)<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONSTRING**</dt> </dl>                      | Versión del producto. Para obtener más información, vea la [**propiedad ProductVersion.**](productversion.md)<br/>                                                                                                                                                                                                                                                                    |



 

Para recuperar el identificador de producto, el propietario registrado o la empresa registrada de las aplicaciones que ya están instaladas, establezca *la* propiedad en uno de los siguientes valores de cadena de texto.



| Valor      | Descripción                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | Identificador del producto. Para obtener más información, vea la [**propiedad ProductID.**](productid.md) |
| RegCompany | La empresa registrada para usar este producto.                                                    |
| RegOwner   | Propietario registrado para usar este producto.                                                      |



 

Para recuperar el tipo de instancia del producto, establezca *la propiedad* en el siguiente valor. Esta propiedad está disponible para productos anunciados o instalados.



| Valor        | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | Un valor que falta o un valor de 0 indica una instalación normal del producto. Un valor de 1 indica un producto instalado mediante una transformación de varias instancias y la [**propiedad MSINEWINSTANCE.**](msinewinstance.md) Disponible con el instalador que ejecuta Windows Server 2003 o Windows XP con SP1. Para obtener más información, [vea Instalación de varias instancias de productos y revisiones.](installing-multiple-instances-of-products-and-patches.md) |



 

Las propiedades de la lista siguiente también se pueden recuperar de las aplicaciones que se anuncian. Estas propiedades no se pueden recuperar para las instancias de producto que se instalan en un contexto no administrado por usuario para cuentas de usuario que no sean cuentas de usuario actuales.



| Propiedades anunciadas                 | Descripción                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TRANSFORMACIONES DE INSTALLPROPERTY \_           | Transformaciones.                                                                                                                                                                                                                                                                                          |
| INSTALLPROPERTY \_ LANGUAGE             | Idioma del producto.                                                                                                                                                                                                                                                                                    |
| INSTALLPROPERTY \_ PRODUCTNAME          | Natural legible: nombre del producto. Para obtener más información, vea la [**propiedad ProductName.**](productname.md)                                                                                                                                                                                              |
| INSTALLPROPERTY \_ ASSIGNMENTTYPE       | Es igual a cero (0) si el producto se anuncia o se instala por usuario. Es igual a uno (1) si el producto se anuncia o se instala por equipo para todos los usuarios.<br/>                                                                                                                                  |
| INSTALLPROPERTY \_ PACKAGECODE          | Identificador del paquete desde el que se instaló este producto. Para obtener más información, vea [Códigos de paquete](package-codes.md).                                                                                                                                                                                      |
| VERSIÓN DE \_ INSTALLPROPERTY              | Versión del producto derivada de la [**propiedad ProductVersion.**](productversion.md)                                                                                                                                                                                                                  |
| INSTALLPROPERTY \_ PRODUCTICON          | Icono principal del paquete. Para obtener más información, vea la [**propiedad ARPPRODUCTICON.**](arpproducticon.md)                                                                                                                                                                                       |
| INSTALLPROPERTY \_ PACKAGENAME          | Nombre del paquete de instalación original.                                                                                                                                                                                                                                                           |
| INSTALLPROPERTY \_ AUTHORIZED \_ LUA \_ APP | Un valor de 1 indica un producto que pueden atender los usuarios que no son administradores mediante la aplicación de revisiones de control de cuentas [de usuario (UAC).](user-account-control--uac--patching.md) Un valor que falta o un valor de 0 indica que la aplicación de revisiones con privilegios mínimos no está habilitada. Disponible con Windows Installer 3.0 y versiones posteriores. |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la llamada se realiza correctamente, la propiedad contiene el valor como una cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-00000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




