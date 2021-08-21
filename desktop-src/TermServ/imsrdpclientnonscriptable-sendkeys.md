---
title: Método SendKeys IMsRdpClientNonScriptable
description: Envía una serie de pulsaciones de tecla al control. Las pulsaciones de tecla están en formato de código de examen, que son los datos del teclado de las teclas físicas reales.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Método SendKeys Servicios de Escritorio remoto
- Método SendKeys Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable
- Interfaz IMsRdpClientNonScriptable Servicios de Escritorio remoto , método SendKeys
- Método SendKeys Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable2
- Interfaz IMsRdpClientNonScriptable2 Servicios de Escritorio remoto , método SendKeys
- Método SendKeys Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto , método SendKeys
- Método SendKeys Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , método SendKeys
- Método SendKeys Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , método SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 530f74bdab808ce6cad6f777d12da932db073ddec022e007eb73fabc538fab20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118855323"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>IMsRdpClientNonScriptable::SendKeys (método)

Envía una serie de pulsaciones de tecla al control. Las pulsaciones de tecla están en formato de código de examen, que son los datos del teclado de las teclas físicas reales.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*numKeys* \[ En\]
</dt> <dd>

Número de pulsaciones de tecla que se envían. El número máximo de claves que se pueden enviar en una operación es 20. El método devuelve **E \_ INVALIDARG** si este parámetro es mayor que 20. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> <dt>

*pbArrayKeyUp* \[ En\]
</dt> <dd>

Matriz cuyo tamaño es igual a *numKeys.* Un elemento es **TRUE si** la clave correspondiente es UP y **FALSE** si la clave correspondiente es DOWN.

</dd> <dt>

*plKeyData* \[ En\]
</dt> <dd>

Matriz cuyo tamaño es igual a *numKeys.* La matriz contiene datos de pulsación de tecla y corresponde al valor del parámetro *lParam* del [mensaje \_ KEYDOWN de WM.](../inputdev/wm-keydown.md) Los datos especifican el recuento de repeticiones, el código de examen, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición. Para obtener una descripción de los bits de esta matriz, vea [WM \_ KEYDOWN](../inputdev/wm-keydown.md).

El elemento correspondiente de *pbArrayKeyUp* indica si la clave es UP o DOWN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

El **método SendKeys** no combina las pulsaciones de tecla realizadas por el usuario local con las pulsaciones de tecla que envía el método. Todas las pulsaciones de tecla que se pasan al método se envían a la sesión remota en una única secuencia atómica.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                               |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable se define como 2f079c4c-87b2-4afd-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[WM \_ KEYDOWN](../inputdev/wm-keydown.md)
</dt> </dl>

 

