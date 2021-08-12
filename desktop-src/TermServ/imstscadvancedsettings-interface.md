---
title: Interfaz IMsTscAdvancedSettings
description: Incluye métodos para recuperar y establecer propiedades que permiten el almacenamiento en caché de mapas de bits, la compresión y el redireccionamiento de impresoras y portapapeles.
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
ms.openlocfilehash: 2f1156f59178275ff9406299fc553afacd3ce99a0488497f836d147ec1d63547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606202"
---
# <a name="imstscadvancedsettings-interface"></a>Interfaz IMsTscAdvancedSettings

Incluye métodos para recuperar y establecer propiedades que permiten el almacenamiento en caché de mapas de bits, la compresión y el redireccionamiento de impresoras y portapapeles. También puede especificar nombres de archivos DLL de cliente de canal virtual.

Para obtener una instancia de esta interfaz, use la [**propiedad IMsTscAx::AdvancedSettings.**](imstscax-advancedsettings.md)

## <a name="members"></a>Miembros

La **interfaz IMsTscAdvancedSettings** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IMsTscAdvancedSettings** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsTscAdvancedSettings** tiene estas propiedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propiedad</th>
<th style="text-align: left;">Tipo de acceso</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el modo de entrada en segundo plano está habilitado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si está habilitado el almacenamiento en caché de mapa de bits.<br/>
<blockquote>
[!Note]<br />
El error ortográfico en el nombre de la propiedad está en la versión publicada del control.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-compress.md"><strong>Comprimir</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si la compresión está habilitada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el modo de pantalla completa que controla el contenedor está habilitado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si está habilitada la redirección de impresoras y portapapeles.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a><br/></td>
<td style="text-align: left;">Solo escritura<br/></td>
<td style="text-align: left;">Especifica el nombre del archivo que contiene los datos de icono a los que se tendrá acceso al mostrar el cliente en modo de pantalla completa.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a><br/></td>
<td style="text-align: left;">Solo escritura<br/></td>
<td style="text-align: left;">Especifica el índice del icono en el archivo de icono actual.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a><br/></td>
<td style="text-align: left;">Solo escritura<br/></td>
<td style="text-align: left;">Especifica el nombre del identificador de configuración regional de entrada activo (anteriormente denominado diseño de teclado) que se usará para la conexión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a><br/></td>
<td style="text-align: left;">Solo escritura<br/></td>
<td style="text-align: left;">Especifica los nombres de los archivos DLL de cliente de canal virtual que se cargarán.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Esta interfaz se ha ampliado mediante las interfaces siguientes, donde cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

