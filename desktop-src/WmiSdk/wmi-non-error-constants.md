---
description: Códigos de retorno de WMI que indican el estado y no indican un error.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Constantes que no son de error de WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276251"
---
# <a name="wmi-non-error-constants"></a>Constantes que no son de error de WMI

Códigos de retorno de WMI que indican el estado y no indican un error.

Si una operación no produce un error, WMI devuelve uno de los códigos siguientes como **HRESULT** que indica el estado de la operación.

> [!Note]  
> Algunos métodos de las clases WMI pueden devolver códigos de error del sistema y de la red (por ejemplo, 64). Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema. Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: el nombre de red especificado ya no está disponible.

 

En C++, puede llamar a [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) y especificar **C: \\ Windows \\ system32 \\ WBEM \\wmiutils.dll** como el módulo de mensajes.

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**NO se ha podido obtener \_ \_ un \_ error de WBEM**
</dt> <dd> <dl> <dt>

0 (0X0)
</dt> <dt>



La operación se realizó correctamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ falso**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



No hay más objetos disponibles, el número de objetos devueltos es menor que el número solicitado o es el final de una enumeración. También se devuelve este valor cuando se llama a este método con un valor de 0 para el parámetro *uCount* .


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ ya \_ existe**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



Se intentó crear un objeto o una clase que ya existe.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_ \_ \_ configuración predeterminada de WBEM \_ S**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Se eliminó una propiedad reemplazada. Se devuelve este valor para indicar que se ha restaurado el valor original no reemplazado como resultado de la eliminación.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ diferente**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Los elementos (objetos, clases, etc.) que se están comparando no son idénticos.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**\_S. \_**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Se agotó el tiempo de espera de una llamada. No se trata de una condición de error. Por lo tanto, es posible que también se hayan devuelto algunos resultados.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ no hay \_ más \_ datos**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



No hay más datos disponibles en la enumeración y el usuario debe finalizar la enumeración.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_operación S de WBEM \_ \_ cancelada**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



La operación se canceló de manera intencionada o accidental.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ pendientes**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Todavía hay una solicitud en curso y los resultados aún no están disponibles.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_ \_ objetos duplicados de WBEM \_**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



Se detectó más de una copia del mismo objeto en el conjunto de resultados de una enumeración.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_ \_ acceso \_ denegado a WBEM**
</dt> <dd> <dl> <dt>

262153 (0x40009)
</dt> <dt>



Al usuario se le denegó el acceso a algunos, pero no a todos los recursos.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ resultados parciales de WBEM S \_**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



El usuario no recibió todos los objetos solicitados debido a recursos inaccesibles (distintos de las infracciones de seguridad).


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_ \_ servicio limitado de WBEM S \_**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



El proveedor es capaz de ofrecer un servicio limitado.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ actualizado indirectamente \_**
</dt> <dd> <dl> <dt>

274434 (0x43002)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>WbemCli. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WbemCli. idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de retorno de WMI](wmi-return-codes.md)
</dt> </dl>

 

