---
description: Define los parámetros de entrada y salida para los métodos.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: __PARAMETERS clase
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
ms.openlocfilehash: a2f39cb7b88977c8f61e562badaa6cbda7a5004fc2d0edf70eb59c6276070efd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110570"
---
# <a name="__parameters-class"></a>\_\_CLASE PARAMETERS

La **\_ \_ clase del** sistema PARAMETERS es una clase abstracta que define los parámetros de entrada y salida para los métodos. También se usa para pasar valores de parámetros de entrada y salida entre un cliente WMI y un proveedor de métodos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase PARAMETERS** no define ningún miembro.

## <a name="remarks"></a>Comentarios

Para definir un método en una clase de usuario, un cliente WMI crea una copia de la clase **\_ \_ PARAMETERS** y agrega una propiedad para cada parámetro de entrada de un método. Si el método contiene un valor devuelto o parámetros de salida, se debe crear otra copia de **\_ \_ PARAMETERS.** Si el método devuelve un valor devuelto, el cliente debe agregar una propiedad denominada **ReturnValue**. A continuación, el proveedor de métodos almacena los parámetros de método con una llamada a [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).

Para invocar un método, un cliente llama a lo siguiente en secuencia:

1.  [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar una copia de la clase **\_ \_ PARAMETERS** almacenada por [**IWbemClassObject::P utMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).
2.  [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance)y, a continuación, establece una propiedad para cada parámetro de entrada en el método .
3.  [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) para ejecutar el método.

Una vez que el método termina de ejecutarse, se puede devolver otra instancia de clase **\_ \_ PARAMETERS** si el método tiene parámetros de salida o un valor devuelto.

-   Si el método se invocó mediante [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), la **\_ \_ instancia PARAMETERS** se devuelve como argumento de salida.
-   Si el método se invocó mediante [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), la instancia **\_ \_ PARAMETERS** se devuelve como un parámetro a [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 




