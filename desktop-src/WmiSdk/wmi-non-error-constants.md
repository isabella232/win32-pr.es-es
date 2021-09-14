---
description: Códigos de retorno wmi que indican el estado y no indican un error.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Constantes de error de WMI (WbemCli.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967016"
---
# <a name="wmi-non-error-constants"></a>Constantes wmi sin errores

Códigos de retorno wmi que indican el estado y no indican un error.

Si una operación no produce un error, WMI devuelve uno de los códigos siguientes como **HRESULT** que indica el estado de la operación.

> [!Note]  
> Algunos métodos de las clases WMI pueden devolver códigos de error del sistema y de red (por ejemplo, 64). Puede comprobar la definición de estos tipos de códigos de error mediante el comando **net helpmsg** en la ventana del símbolo del sistema. Por ejemplo, el comando **net helpmsg 64** devuelve el mensaje: El nombre de red especificado ya no está disponible.

 

En C++, puede llamar a [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) y especificar **C: \\ Windows \\ System32 \\ wbem \\wmiutils.dll** como módulo de mensaje.

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ NO \_ ERROR**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



La operación se realizó correctamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ FALSE**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



No hay más objetos disponibles, el número de objetos devueltos es menor que el número solicitado o este es el final de una enumeración. Este valor también se devuelve cuando se llama a este método con un valor de 0 para el *parámetro uCount.*


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ YA \_ EXISTE**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



Se intentó crear un objeto o clase que ya existe.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM \_ S \_ RESET \_ TO \_ DEFAULT**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Se eliminó una propiedad reemplazada. Este valor se devuelve para indicar que el valor original no invalidado se ha restaurado como resultado de la eliminación.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ DIFFERENT**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Los elementos (objetos, clases, entre otros) que se comparan no son idénticos.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ S \_ TIMEDOUT**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Se ha pasado el tiempo de espera de una llamada. No se trata de una condición de error. Por lo tanto, es posible que también se hayan devuelto algunos resultados.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ NO \_ MORE \_ DATA**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



No hay más datos disponibles en la enumeración y el usuario debe finalizar la enumeración.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**OPERACIÓN DE WBEM \_ \_ \_ CANCELADA**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



La operación se canceló intencionada o involuntaramente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ PENDING**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Una solicitud todavía está en curso y los resultados aún no están disponibles.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM \_ S \_ DUPLICATE \_ OBJECTS**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



Se detectó más de una copia del mismo objeto en el conjunto de resultados de una enumeración.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**ACCESO DE WBEM \_ S \_ \_ DENEGADO**
</dt> <dd> <dl> <dt>

262153 (0x40009)
</dt> <dt>



Al usuario se le denegó el acceso a algunos recursos, pero no a todos.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**RESULTADOS \_ PARCIALES DE WBEM \_ \_**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



El usuario no recibió todos los objetos solicitados debido a recursos inaccesibles (que no son infracciones de seguridad).


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM \_ S \_ LIMITED \_ SERVICE**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



El proveedor es capaz de ofrecer un servicio limitado.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM \_ S \_ ACTUALIZADOS INDIRECTAMENTE \_**
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
| Encabezado<br/>                   | <dl> <dt>WbemCli.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WbemCli.idl</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Códigos de retorno wmi](wmi-return-codes.md)
</dt> </dl>

 

