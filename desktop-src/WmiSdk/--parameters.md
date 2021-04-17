---
description: Define los parámetros de entrada y salida para los métodos.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697254"
---
# <a name="__parameters-class"></a>\_\_Parameters (clase)

La clase de sistema **\_ \_ Parameters** es una clase abstracta que define los parámetros de entrada y salida para los métodos. También se utiliza para pasar los valores de los parámetros de entrada y salida entre un cliente WMI y un proveedor de métodos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ Parameters** no define ningún miembro.

## <a name="remarks"></a>Observaciones

Para definir un método en una clase de usuario, un cliente WMI crea una copia de la clase **\_ \_ Parameters** y agrega una propiedad para cada parámetro de entrada de un método. Si el método contiene un valor devuelto o parámetros de salida, se debe crear otra copia de **\_ \_ los parámetros** . Si el método devuelve un valor devuelto, el cliente debe agregar una propiedad denominada **ReturnValue**. A continuación, el proveedor de métodos almacena los parámetros de método con una llamada a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Para invocar un método, un cliente llama a lo siguiente en secuencia:

1.  [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar una copia de la clase **\_ \_ Parameters** almacenada por [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).
2.  [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)y, a continuación, establece una propiedad para cada parámetro de entrada para el método.
3.  [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para ejecutar el método.

Una vez finalizada la ejecución del método, se puede devolver otra instancia de la clase **\_ \_ Parameters** si el método tiene parámetros de salida o un valor devuelto.

-   Si el método se invocó mediante [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), la instancia de **\_ \_ Parameters** se devuelve como un argumento de salida.
-   Si el método se invocó mediante [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), la instancia de **\_ \_ Parameters** se devuelve como un parámetro a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 




