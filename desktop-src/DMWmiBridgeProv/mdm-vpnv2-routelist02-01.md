---
title: MDM_VPNv2_RouteList02_01 clase
description: La clase MDM \_ VPNv2 \_ RouteList02 01 contiene una lista opcional de rutas que se agregarán a la tabla de enrutamiento de \_ la interfaz VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01 clase
- MDM_VPNv2_RouteList02_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ea9725d70d3acfe4e6831d1d386aedecfd9374728b103d50b67aa15cb61ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750275"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>Clase \_ MDM VPNv2 \_ RouteList02 \_ 01

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

La **clase MDM \_ VPNv2 \_ RouteList02 \_ 01** contiene una lista opcional de rutas que se agregarán a la tabla de enrutamiento de la interfaz VPN.

Esto es necesario para el caso de tunelización dividida en el que el sitio del servidor VPN tiene más subredes que la subred predeterminada en función de la dirección IP asignada a la interfaz.

Cada equipo que ejecuta TCP/IP realiza decisiones de enrutamiento. Estas decisiones están controladas por la tabla de enrutamiento IP. Al agregar valores en este nodo, se actualiza la tabla de enrutamiento con rutas para la conexión posterior a la interfaz VPN. Los valores de este nodo representan el prefijo de destino de las rutas IP. Un prefijo de destino consta de un prefijo de dirección IP y una longitud de prefijo.

La adición de una ruta aquí permite a la pila de redes identificar el tráfico que debe pasar a través de la interfaz VPN para la VPN de túnel dividido. Algunos servidores VPN pueden configurar esto durante la negociación de conexión y no necesitan esta información en el perfil de VPN. Póngase en contacto con el administrador del servidor VPN para determinar si necesita esta información en el perfil de VPN.

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a>Miembros

La **clase \_ MDM VPNv2 \_ RouteList02 \_ 01** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ MDM VPNv2 \_ RouteList02 \_ 01** tiene estas propiedades.

<dl> <dt>

[Dirección](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"

</dd> <dt>

[PrefixSize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Uso de scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

