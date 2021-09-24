---
title: MDM_RemoteWipe clase
description: La clase \_ RemoteWipe de MDM permite un borrado remoto de un dispositivo.
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- MDM_RemoteWipe clase
- MDM_RemoteWipe clase, descrita
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ca943ed0b226f9006733b3e9d8745172cfe9e08
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520062"
---
# <a name="mdm_remotewipe-class"></a>\_Clase RemoteWipe de MDM

> [!NOTE]
> **Parte de la información hace referencia al producto de versión preliminar, el cual puede sufrir importantes modificaciones antes de que se publique la versión comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.**

La **clase \_ RemoteWipe** de MDM permite un borrado remoto de un dispositivo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a>Miembros

La **clase \_ RemoteWipe** mdm tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ RemoteWipe de MDM** tiene estos métodos.

| Método                                              | Descripción                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [**doWipeMethod**](mdm-remotewipe-dowipemethod.md) | Desencadena el dispositivo para iniciar el borrado remoto. |
| [**doWipePersistProvisionedDataMethod**](mdm-remotewipe-dowipepersistprovisioneddatamethod.md) | Desencadena el dispositivo para realizar una copia de seguridad de los datos de aprovisionamiento en una ubicación persistente y realizar un borrado remoto en el dispositivo. La información de la que se ha hecho una copia de seguridad se restaurará y se aplicará al dispositivo cuando se reanude. |
| [**doWipePersistUserDataMethod**](mdm-remotewipe-dowipepersistuserdatamethod.md) | Desencadena el dispositivo para iniciar el borrado remoto mientras se conservan los datos y las cuentas de usuario. |
| [**doWipeProtectedMethod**](mdm-remotewipe-dowipeprotectedmethod.md) | Desencadena el dispositivo para iniciar el borrado remoto en el dispositivo y limpiar completamente la unidad interna. En algunas configuraciones de dispositivo, este comando puede dejar que el dispositivo no pueda arrancar. |

### <a name="properties"></a>Propiedades

La **clase \_ Mdm RemoteWipe** tiene estas propiedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica el nombre del nodo primario. Para esta clase, la cadena es "RemoteWipe".

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Describe la ruta de acceso completa al nodo primario. Para esta clase, la cadena es "./Vendor/MSFT/"

</dd> </dl>

## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo usar RemoteWipe e invocar doWipeMethod.

> [!Note]  
> Este ejemplo debe ejecutarse en el usuario del sistema local. Para ello, descargue la herramienta psexec desde y <https://technet.microsoft.com/sysinternals/bb897553.aspx> ejecute desde un símbolo del sistema de administración con `psexec.exe -i -s cmd.exe` privilegios elevados.

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible | \[Windows 10 solo aplicaciones de escritorio\]                                                    |
| Servidor mínimo compatible | No se admite ninguno                                                                      |
| Espacio de nombres                | DMMap \\ de MDM de CIMv2 \\ \\ raíz                                                             |
| MOF                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>
