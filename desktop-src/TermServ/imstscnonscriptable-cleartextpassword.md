---
title: Propiedad ClearTextPassword de IMsTscNonScriptable
description: Establece la Escritorio remoto contraseña del control ActiveX en formato de texto simple.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsTscNonScriptable, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803794"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>IMsTscNonScriptable:: ClearTextPassword (propiedad)

Establece la Escritorio remoto contraseña del control ActiveX en formato de texto simple.

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Valor de propiedad

Contraseña que se va a usar para conectarse, especificada en formato de texto simple.

## <a name="error-codes"></a>Códigos de error

Vuelva **a \_ Aceptar si es** correcto.

## <a name="remarks"></a>Observaciones

La contraseña se pasa al servidor en el canal de comunicaciones RDP cifrado de forma segura. Después de establecer una contraseña de texto sin formato, no se puede recuperar en formato de texto no cifrado.

La propiedad **ClearTextPassword** solo se puede establecer cuando el control ActiveX escritorio remoto no está en estado conectado. Si se establece esta propiedad, se producirá un error si el control está conectado. Para comprobar el estado conectado, recupere la propiedad [**IMsTscAx:: Connected**](imstscax-connected.md) .

También puede llamar a este método para establecer una contraseña de texto no cifrado antes de convertirla en una contraseña codificada portable o en una contraseña codificada binaria (no portable). Sin embargo, tenga en cuenta que las contraseñas codificadas no se deben considerar cifradas de forma segura.

Si llama primero a este método para establecer una contraseña en formato de texto simple, puede convertir la contraseña al formato codificado.

**Para convertir una contraseña de texto no cifrado en formato codificado**

1.  Establezca la contraseña en formato de texto no cifrado en la propiedad **ClearTextPassword** .
2.  Para recuperar la contraseña en formato codificado binario (no portable), recupere la propiedad [**BinaryPassword**](imstscnonscriptable-binarypassword.md) y las propiedades [**BinarySalt**](imstscnonscriptable-binarysalt.md) . Tanto la parte de la contraseña codificada como la parte del valor Salt son necesarias para establecer una contraseña en formato codificado binario.
3.  Para recuperar la contraseña en formato codificado portable, recupere el método [**PortablePassword**](imstscnonscriptable-portablepassword.md) y las propiedades [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Ambas partes son necesarias para establecer una contraseña en formato codificado portátil.

Después de seguir los tres pasos anteriores, puede establecer la contraseña en formato codificado estableciendo las propiedades [**BinaryPassword**](imstscnonscriptable-binarypassword.md) y [**BinarySalt**](imstscnonscriptable-binarysalt.md) , o [**PortablePassword**](imstscnonscriptable-portablepassword.md) y [**PortableSalt**](imstscnonscriptable-portablesalt.md) . Ambas partes son obligatorias.

Para habilitar el inicio de sesión automático, también debe establecer las propiedades de [**nombre de usuario**](imstscax-username.md) y [**dominio**](imstscax-domain.md) . Si la contraseña no puede autenticar al usuario, el cuadro de diálogo de inicio de sesión de Windows se muestra en el servidor para pedir la contraseña al usuario.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





