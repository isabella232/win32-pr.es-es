---
description: Las propiedades de información de dispositivos son propiedades que describen la instalación y la instalación del dispositivo.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Constantes de propiedad de información del dispositivo (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715169"
---
# <a name="device-information-property-constants"></a>Constantes de propiedades de información del dispositivo

Las propiedades de información de dispositivos son propiedades que describen la instalación y la instalación del dispositivo. Estas propiedades están disponibles a través de las interfaces [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) y también a través del elemento raíz. Las propiedades de información del dispositivo tienen el prefijo "WIA \_ DIP \_ " (propiedad de información del dispositivo) y se proporcionan mediante la adquisición de imágenes de Windows (WIA). Con fines de scripting, estas constantes usan el prefijo "DeviceInfo" y forman parte del tipo enumerado [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) . El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </dl></td>
<td style="text-align: left;">Cadena de identificador de dispositivo para el minicontrolador WIA. El servicio WIA crea y mantiene esta propiedad.<br/> Tipo: VT_BSTR, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </dl></td>
<td style="text-align: left;">Cadena de Descripción del proveedor para el minicontrolador WIA. La descripción del proveedor se obtiene del archivo INF. Una aplicación Lee esta propiedad para obtener una descripción del proveedor del dispositivo. El servicio WIA crea y mantiene esta propiedad.<br/> Tipo: VT_BSTR, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </dl></td>
<td style="text-align: left;">Cadena de Descripción del dispositivo para el minicontrolador WIA. El servicio WIA crea y mantiene esta propiedad. La cadena de Descripción del dispositivo que contiene esta propiedad se obtiene del archivo INF. Una aplicación Lee esta propiedad para obtener una descripción del dispositivo.<br/> Tipo: VT_BSTR, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </dl></td>
<td style="text-align: left;">El tipo de dispositivo y el subtipo de dispositivo. El servicio WIA crea y mantiene esta propiedad. Use la macro GET_STIDEVICE_TYPE para obtener el tipo de dispositivo. El tipo de dispositivo y el subtipo se obtienen del archivo INF. Una aplicación Lee esta propiedad para determinar si usa un escáner, cámara o dispositivo de vídeo.<br/> Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> Actualmente, los tipos de dispositivo se definen como se indica a continuación. El asterisco * indica que el tipo de dispositivo no es compatible con Windows Vista y versiones posteriores. El doble asterisco * * indica que el tipo de dispositivo no es compatible con Windows Server 2003, Windows Vista o posterior. <br/> 
<table>
<thead>
<tr class="header">
<th>Tipo</th>
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>StiDeviceTypeDefault</td>
<td>0x0000</td>
<td>Dispositivo predeterminado</td>
</tr>
<tr class="even">
<td>StiDeviceTypeScanner</td>
<td>0x0001</td>
<td>Dispositivo de escáner (vea la <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> para determinar si el escáner está plano o está alimentado por hojas).</td>
</tr>
<tr class="odd">
<td>StiDeviceTypeDigitalCamera*</td>
<td>0x0002</td>
<td>Dispositivo de cámara</td>
</tr>
<tr class="even">
<td>StiDeviceTypeStreamingVideo**</td>
<td>0x0003</td>
<td>Dispositivo de vídeo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </dl></td>
<td style="text-align: left;"><p>El nombre de puerto del dispositivo instalado, asignado por el controlador de modo kernel que funciona el dispositivo. El servicio WIA crea y mantiene esta propiedad. Una aplicación Lee esta propiedad para determinar el nombre del puerto.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </dl></td>
<td style="text-align: left;"><p>Nombre del dispositivo. El servicio WIA crea y mantiene esta propiedad. El nombre del dispositivo incluido en esta propiedad se obtiene del archivo INF. Una aplicación Lee esta propiedad para obtener el nombre del dispositivo.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </dl></td>
<td style="text-align: left;"><p>Nombre del servidor en el que se está ejecutando el minicontrolador WIA. Esta propiedad es opcional para Windows XP y versiones posteriores.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </dl></td>
<td style="text-align: left;"><p>El identificador de dispositivo del dispositivo WIA instalado en un equipo remoto. El servicio WIA crea y mantiene esta propiedad. El servicio WIA solo lo usa internamente.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </dl></td>
<td style="text-align: left;"><p>El CLSID proporcionado por el proveedor para cualquier objeto COM de extensión de la interfaz de usuario que se instala con el minicontrolador WIA. El servicio WIA crea y mantiene esta propiedad. El valor CLSID de la interfaz de usuario contenido en esta propiedad se obtiene del archivo INF. Si no se especifica ningún CLSID de interfaz de usuario, el servicio WIA proporciona un valor predeterminado. Esta propiedad solo la usa internamente el servicio WIA cuando se muestra la interfaz de usuario.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </dl></td>
<td style="text-align: left;"><p>El tipo de conexión que usa el dispositivo. El servicio WIA crea y mantiene esta propiedad y solo el servicio WIA puede cambiarla.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>La propiedad puede tener los siguientes valores posibles.</p>

<table>
<thead>
<tr class="header">
<th>Value</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Dispositivo WDM genérico</td>
</tr>
<tr class="even">
<td>2</td>
<td>Dispositivo SCSI</td>
</tr>
<tr class="odd">
<td>4</td>
<td>Dispositivo USB</td>
</tr>
<tr class="even">
<td>8</td>
<td>Dispositivo serie</td>
</tr>
<tr class="odd">
<td>16</td>
<td>Dispositivo paralelo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </dl></td>
<td style="text-align: left;"><p>La configuración de la velocidad en baudios actual para el dispositivo. El servicio WIA crea y mantiene esta propiedad. El valor debe estar &quot; vacío &quot; si el dispositivo no está conectado mediante un cable serie.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </dl></td>
<td style="text-align: left;"><p>Las capacidades de STI genéricas para el dispositivo que se obtienen del archivo INF. El servicio WIA crea y mantiene esta propiedad. Una aplicación Lee esta propiedad para determinar las funciones STI genéricas del dispositivo.</p>
<p>Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </dl></td>
<td style="text-align: left;"><p>Número (como cadena) de la versión de WIA actual que está instalada en el sistema. Una aplicación Lee esta propiedad para determinar la versión de WIA que está instalada en el sistema. El servicio WIA crea y mantiene esta propiedad. Esta propiedad está disponible en Windows XP y versiones posteriores.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>Versión del archivo DLL actual del minicontrolador WIA. El servicio WIA crea y mantiene esta propiedad. Esta propiedad está disponible en Windows XP y versiones posteriores.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </dl></td>
<td style="text-align: left;"><p>Identificador de PnP actual para el dispositivo. El servicio WIA crea y mantiene esta propiedad. Esta propiedad está disponible en Windows Vista y versiones posteriores.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </dl></td>
<td style="text-align: left;"><p>Versión del controlador STI genérico. El servicio WIA crea y mantiene esta propiedad. Una aplicación Lee esta propiedad para determinar la versión del controlador STI genérico. Esta propiedad está disponible en Windows Vista y versiones posteriores.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




