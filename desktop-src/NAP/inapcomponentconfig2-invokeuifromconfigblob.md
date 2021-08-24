---
title: Método INapComponentConfig2 InvokeUIFromConfigBlob (NapCommon.h)
description: Se implementa mediante validadores de estado del sistema (SHV) según sea necesario para cargar la configuración de un equipo remoto o local en memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración.
ms.assetid: 9c012690-6751-4a47-8683-74abac610c77
keywords:
- Método NAP InvokeUIFromConfigBlob
- Método NAP InvokeUIFromConfigBlob , interfaz INapComponentConfig2
- INapComponentConfig2 interface NAP , InvokeUIFromConfigBlob (método)
topic_type:
- apiref
api_name:
- INapComponentConfig2.InvokeUIFromConfigBlob
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d85e0506b8adf084b65a13a117a9dea3856fcff2e73f65a229bdb31b283fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803165"
---
# <a name="inapcomponentconfig2invokeuifromconfigblob-method"></a>Método INapComponentConfig2::InvokeUIFromConfigBlob

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Los validadores de estado del sistema (SHV) implementan el método **InvokeUIFromConfigBlob** según sea necesario para cargar la configuración de un equipo remoto o local en memoria y mostrar una interfaz de usuario que permita la manipulación de los datos de configuración. El componente de configuración debe admitir el uso de [**INapComponentConfig a**](inapcomponentconfig.md) través de DCOM.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT InvokeUIFromConfigBlob(
  [in, unique] HWND   hwndParent,
  [in]         UINT16 inbCount,
  [in]         BYTE   *inData,
  [out]        UINT16 *outbCount,
  [out]        BYTE   **outdata,
  [out]        BOOL   *fConfigChanged
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwndParent* \[ En\]
</dt> <dd>

Identificador de la ventana principal o del propietario. Se debe proporcionar un identificador de ventana válido.

</dd> <dt>

*inbCount* \[ En\]
</dt> <dd>

Tamaño, en bytes, de *inData*.

</dd> <dt>

*inData* \[ En\]
</dt> <dd>

Puntero a un búfer que almacena los datos de configuración iniciales. Estos datos se exportan desde el equipo remoto o local.

</dd> <dt>

*outbCount* \[ out\]
</dt> <dd>

Tamaño, en bytes, de *outdata*.

</dd> <dt>

*outdata* \[ out\]
</dt> <dd>

Puntero a un búfer que almacena los datos de configuración modificados por la interfaz de usuario de configuración de SHV. El equipo remoto o local importa estos datos.

</dd> <dt>

*fConfigChanged* \[ out\]
</dt> <dd>

Puntero a un **bool** que se establece en **TRUE** si la configuración se cambió durante la operación de interfaz de usuario y **FALSE en caso** contrario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o uno de los códigos de error Windows estándar.

## <a name="remarks"></a>Comentarios

Si se usa para una máquina local, esta función se puede usar para la configuración de SHV por directiva. Proporciona una manera de invocar una interfaz de usuario de SHV y editar una configuración de SHV existente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>NapCommon.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon.idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INapComponentConfig2**](inapcomponentconfig2.md)
</dt> </dl>

 

 





