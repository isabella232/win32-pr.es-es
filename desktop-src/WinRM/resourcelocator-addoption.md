---
title: Método ResourceLocator. AddOption (WSManDisp. h)
description: Agrega datos adicionales necesarios para procesar la solicitud. Por ejemplo, algunos proveedores de WMI pueden requerir un objeto IWbemContext o SWbemNamedValueSet con información específica del proveedor.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Método AddOption Administración remota de Windows
- Método AddOption Administración remota de Windows, objeto ResourceLocator
- Administración remota de Windows de objeto ResourceLocator, método AddOption
topic_type:
- apiref
api_name:
- ResourceLocator.AddOption
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f400dd2c59d2395dd2755846245f4e4ad385e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079021"
---
# <a name="resourcelocatoraddoption-method"></a>ResourceLocator. AddOption, método

Agrega datos adicionales necesarios para procesar la solicitud. Por ejemplo, algunos proveedores de WMI pueden requerir un objeto [**IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) con información específica del proveedor. Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objetos de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Sintaxis


```VB
ResourceLocator.AddOption( _
  ByVal OptionName, _
  ByVal OptionValue, _
  ByVal mustComply _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OptionName* \[ de\]
</dt> <dd>

Nombre (clave) del objeto de datos opcional.

</dd> <dt>

*OptionValue* \[ de\]
</dt> <dd>

Valor proporcionado para el objeto de datos opcional.

</dd> <dt>

*mustComply* \[ de\]
</dt> <dd>

Marca que indica que la opción se debe procesar. El valor predeterminado es **false** (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

**IWSManResourceLocator:: AddOption** es el método de C++ correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

