---
title: Interfaz IMsTscAdvancedSettings
description: Incluye métodos para recuperar y establecer propiedades que permiten el almacenamiento en caché de mapas de bits, la compresión y la redirección de impresoras y portapapeles.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Interfaz IMsTscAdvancedSettings Servicios de Escritorio remoto
- Interfaz IMsTscAdvancedSettings Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc379375456feb5de50abdc68ff2cc2da463fbe
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475351"
---
# <a name="imstscadvancedsettings-interface"></a>Interfaz IMsTscAdvancedSettings

Incluye métodos para recuperar y establecer propiedades que permiten el almacenamiento en caché de mapas de bits, la compresión y la redirección de impresoras y portapapeles. También puede especificar nombres de archivos DLL de cliente de canal virtual.

Puede obtener una instancia de esta interfaz mediante la [**propiedad IMsTscAx::AdvancedSettings.**](imstscax-advancedsettings.md)

## <a name="members"></a>Miembros

La **interfaz IMsTscAdvancedSettings** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsTscAdvancedSettings** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsTscAdvancedSettings** tiene estas propiedades.




| Propiedad | Tipo de acceso | Descripción | 
|----------|-------------|-------------|
| <a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a><br /> | Lectura/escritura<br /> | Especifica si el modo de entrada en segundo plano está habilitado.<br /> | 
| <a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a><br /> | Lectura/escritura<br /> | Especifica si está habilitado el almacenamiento en caché de mapa de bits.<br /><blockquote>[!Note]<br />El error ortográfico en el nombre de la propiedad está en la versión publicada del control.</blockquote><br /> | 
| <a href="imstscadvancedsettings-compress.md"><strong>Comprimir</strong></a><br /> | Lectura/escritura<br /> | Especifica si la compresión está habilitada.<br /> | 
| <a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a><br /> | Lectura/escritura<br /> | Especifica si el modo de pantalla completa con control de contenedor está habilitado.<br /> | 
| <a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a><br /> | Lectura/escritura<br /> | Especifica si está habilitada la redirección de impresoras y portapapeles.<br /> | 
| <a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a><br /> | Solo escritura<br /> | Especifica el nombre del archivo que contiene los datos de icono a los que se tendrá acceso al mostrar el cliente en modo de pantalla completa.<br /> | 
| <a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a><br /> | Solo escritura<br /> | Especifica el índice del icono en el archivo de icono actual.<br /> | 
| <a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a><br /> | Solo escritura<br /> | Especifica el nombre del identificador de configuración regional de entrada activa (anteriormente denominado diseño de teclado) que se usará para la conexión.<br /> | 
| <a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a><br /> | Solo escritura<br /> | Especifica los nombres de los archivos DLL de cliente de canal virtual que se cargarán.<br /> | 




 

## <a name="remarks"></a>Comentarios

Esta interfaz se ha ampliado mediante las interfaces siguientes, y cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

