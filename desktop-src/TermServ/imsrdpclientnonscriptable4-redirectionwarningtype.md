---
title: Propiedad RedirectionWarningType de IMsRdpClientNonScriptable4
description: Controla la presencia y la apariencia del cuadro de diálogo que notifica al usuario sobre la redirección.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType
- Propiedad RedirectionWarningType Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad RedirectionWarningType
- Propiedad RedirectionWarningType Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad RedirectionWarningType
- Servicios de Escritorio remoto de la propiedad RedirectionWarningType, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad RedirectionWarningType
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686028"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a>IMsRdpClientNonScriptable4:: RedirectionWarningType (propiedad)

Controla la presencia y la apariencia del cuadro de diálogo que notifica al usuario sobre la redirección.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a>Valor de propiedad

Establece el tipo del cuadro de diálogo que notifica al usuario de la redirección.

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)


</dt> <dd>

El cuadro de diálogo no es específico del editor.

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)


</dt> <dd>

El cuadro de diálogo es para archivos sin firmar.

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)


</dt> <dd>

El cuadro de diálogo es para un publicador desconocido.

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)


</dt> <dd>

El cuadro de diálogo es para los archivos del usuario.

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)


</dt> <dd>

El cuadro de diálogo se muestra para archivos firmados con certificado de terceros.

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)


</dt> <dd>

No se muestra el cuadro de diálogo porque la aplicación está publicada por un editor de confianza.

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)


</dt> <dd>

No se muestra el cuadro de diálogo porque la aplicación está publicada por un editor de confianza.

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

El valor **RedirectionWarningTypeDefault**, que es el valor predeterminado de esta propiedad, no ejerce ningún control sobre el cuadro de diálogo. En este caso, la propiedad de control es [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) en [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





