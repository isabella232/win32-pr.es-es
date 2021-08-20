---
title: Método ResourceLocator.AddOption (WSManDisp.h)
description: Agrega datos adicionales necesarios para procesar la solicitud. Por ejemplo, algunos proveedores WMI pueden requerir un objeto IWbemContext o SWbemNamedValueSet con información específica del proveedor.
ms.assetid: c85949fc-41e7-47eb-8aab-9b456490bc81
ms.tgt_platform: multiple
keywords:
- Método AddOption Windows Remote Management
- Método AddOption Windows administración remota , objeto ResourceLocator
- Objeto ResourceLocator Windows Remote Management , método AddOption
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
ms.openlocfilehash: 2c03e587c4884e6d9efc3b98bdd7b41b4204a783e153d9e59a400a4e4bc02a65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112970"
---
# <a name="resourcelocatoraddoption-method"></a>Método ResourceLocator.AddOption

Agrega datos adicionales necesarios para procesar la solicitud. Por ejemplo, algunos proveedores WMI pueden requerir un [**objeto IWbemContext**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext) o [**SWbemNamedValueSet**](/windows/desktop/WmiSdk/swbemnamedvalueset) con información específica del proveedor. Puede proporcionar un objeto [**ResourceLocator**](resourcelocator.md) en lugar de especificar un URI de recurso en operaciones de objeto [**de**](session.md) sesión como [**Session.Get**](session-get.md), [**Session.Put**](session-put.md)o [**Session.Enumerate.**](session-enumerate.md)

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

*OptionName* \[ En\]
</dt> <dd>

Nombre (clave) del objeto de datos opcional.

</dd> <dt>

*OptionValue* \[ En\]
</dt> <dd>

Valor proporcionado para el objeto de datos opcional.

</dd> <dt>

*mustComply* \[ En\]
</dt> <dd>

Marca que indica que se debe procesar la opción. El valor predeterminado **es False** (0).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

**IWSManResourceLocator::AddOption es** el método de C++ correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

