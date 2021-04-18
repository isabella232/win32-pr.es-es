---
title: IMsRdpClientNonScriptable SendKeys (método)
description: Envía una serie de pulsaciones de teclas al control. Las pulsaciones de teclas están en formato de código de examen, que son los datos de teclado de las claves físicas reales.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Método SendKeys Servicios de Escritorio remoto
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, método SendKeys
- Método SendKeys Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, método SendKeys
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
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491657"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>IMsRdpClientNonScriptable:: SendKeys (método)

Envía una serie de pulsaciones de teclas al control. Las pulsaciones de teclas están en formato de código de examen, que son los datos de teclado de las claves físicas reales.

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

*numKeys* \[ de\]
</dt> <dd>

Número de pulsaciones de tecla que se van a enviar. El número máximo de claves que se pueden enviar en una operación es 20. El método devuelve **E \_ INVALIDARG** si este parámetro es mayor que 20. Para obtener más información, vea la sección Comentarios que se muestra más adelante.

</dd> <dt>

*pbArrayKeyUp* \[ de\]
</dt> <dd>

Matriz cuyo tamaño es igual a *numKeys*. Un elemento es **true** si la tecla correspondiente está activa y **false** si la tecla correspondiente está fuera de la actividad.

</dd> <dt>

*plKeyData* \[ de\]
</dt> <dd>

Matriz cuyo tamaño es igual a *numKeys*. La matriz contiene datos de pulsación de teclas y corresponde al valor del parámetro *lParam* del mensaje de [ \_ KEYDOWN de WM](../inputdev/wm-keydown.md) . Los datos especifican el número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición. Para obtener una descripción de los bits de esta matriz, vea la muestra de [WM \_ ](../inputdev/wm-keydown.md).

El elemento correspondiente en *pbArrayKeyUp* indica si la tecla está arriba o abajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

El método **SendKeys** no combina las pulsaciones de teclas realizadas por el usuario local con pulsaciones de teclas que el método está enviando. Todas las pulsaciones de tecla que se pasan al método se envían a la sesión remota en una sola secuencia atómica.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

[KEYDOWN de WM \_](../inputdev/wm-keydown.md)
</dt> </dl>

 

