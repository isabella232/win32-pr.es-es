---
title: Propiedad ClearTextPassword IMsTscNonScriptable
description: Establece la contraseña Escritorio remoto ActiveX control en formato de texto no cifrado.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Propiedad ClearTextPassword Servicios de Escritorio remoto
- Propiedad ClearTextPassword Servicios de Escritorio remoto , interfaz IMsTscNonScriptable
- Interfaz IMsTscNonScriptable Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable
- Interfaz IMsRdpClientNonScriptable Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable2
- Interfaz IMsRdpClientNonScriptable2 Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , objeto MsRdpClient6
- Objeto MsRdpClient6 Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , objeto MsRdpClient7
- Objeto MsRdpClient7 Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , objeto MsRdpClient8
- Objeto MsRdpClient8 Servicios de Escritorio remoto , propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto , objeto MsRdpClient9
- Objeto MsRdpClient9 Servicios de Escritorio remoto , propiedad ClearTextPassword
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
ms.openlocfilehash: 0519e7379eab529cc5275c85a11116764417d524a03dff2e1eab74a914b6560b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125055"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a>Propiedad IMsTscNonScriptable::ClearTextPassword

Establece la contraseña Escritorio remoto ActiveX control en formato de texto no cifrado.

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a>Valor de propiedad

Contraseña que se va a usar para conectarse, especificada en formato de texto no cifrado.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Comentarios

La contraseña se pasa al servidor en el canal de comunicaciones RDP cifrado de forma segura. Una vez establecida una contraseña de texto no cifrado, no se puede recuperar en formato de texto no cifrado.

La **propiedad ClearTextPassword** solo se puede establecer cuando el control Escritorio remoto ActiveX no está en el estado conectado. Se produce un error al establecer esta propiedad si el control está conectado. Para comprobar el estado conectado, recupere la [**propiedad IMsTscAx::Connected.**](imstscax-connected.md)

También puede llamar a este método para establecer una contraseña de texto no cifrado antes de convertirla en una contraseña codificada portable o en una contraseña codificada binaria (noportable). Sin embargo, tenga en cuenta que las contraseñas codificadas no deben considerarse cifradas de forma segura.

Si primero llama a este método para establecer una contraseña en formato de texto no cifrado, puede convertir la contraseña al formato codificado.

**Para convertir una contraseña de texto no cifrado al formato codificado**

1.  Establezca la contraseña en formato de texto no cifrado en **la propiedad ClearTextPassword.**
2.  Para recuperar la contraseña en formato codificado binario (noportable), recupere la [**propiedad BinaryPassword**](imstscnonscriptable-binarypassword.md) y las [**propiedades BinarySalt.**](imstscnonscriptable-binarysalt.md) Tanto la parte de contraseña codificada como la parte sal son necesarias para establecer una contraseña en formato binario codificado.
3.  Para recuperar la contraseña en formato codificado portable, recupere el [**método PortablePassword**](imstscnonscriptable-portablepassword.md) y las [**propiedades PortableSalt.**](imstscnonscriptable-portablesalt.md) Ambas partes son necesarias para establecer una contraseña en formato codificado portátil.

Después de seguir los tres pasos anteriores, puede establecer la contraseña en formato codificado estableciendo las propiedades [**BinaryPassword**](imstscnonscriptable-binarypassword.md) y [**BinarySalt,**](imstscnonscriptable-binarysalt.md) o las propiedades [**PortablePassword**](imstscnonscriptable-portablepassword.md) y [**PortableSalt.**](imstscnonscriptable-portablesalt.md) Ambas partes son necesarias.

Para habilitar el inicio de sesión automático, también debe establecer las [**propiedades UserName**](imstscax-username.md) [**y Domain.**](imstscax-domain.md) Si la contraseña no puede autenticar al usuario, se muestra Windows cuadro de diálogo Inicio de sesión en el servidor para solicitar al usuario la contraseña.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832a-0dd06c1c7a0e<br/> |



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

 

 





