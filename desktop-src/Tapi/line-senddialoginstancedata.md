---
description: El mensaje SENDDIALOGINSTANCEDATA de la línea de TSPI \_ hace que TAPI llame a la \_ función PROVIDERGENERICDIALOGDATA de TUISPI en la dll de la interfaz de usuario asociada a htDlgInst, pasándole el bloque de parámetros al que apunta lpParams, de longitud de dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Mensaje de LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690976"
---
# <a name="line_senddialoginstancedata-message"></a>Mensaje de línea \_ SENDDIALOGINSTANCEDATA

El mensaje **\_ SENDDIALOGINSTANCEDATA** de la línea de TSPI hace que TAPI llame a la función [**\_ PROVIDERGENERICDIALOGDATA de TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) en la dll de la interfaz de usuario asociada a *htDlgInst*, pasándole el bloque de parámetros al que apunta *lpParams*, de longitud de *dwSize*.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htDlgInst* 
</dt> <dd>

HTAPIDIALOGINSTANCE que se devolvió al proveedor de servicios cuando la instancia del cuadro de diálogo se creó con la [**línea \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).

</dd> <dt>

*lpParams* 
</dt> <dd>

Puntero a un bloque de parámetros específico del proveedor que se transmite a la función [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) de la dll de la interfaz de usuario, cuyo tamaño se especifica en *dwSize*. Si este parámetro se establece en **null**, se trata de una solicitud para cerrar el cuadro de diálogo inmediatamente y limpiar (el archivo dll de la interfaz de usuario no debe invocar [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante esta limpieza).

</dd> <dt>

*dwSize* 
</dt> <dd>

Tamaño en bytes del bloque de parámetros que se va a transmitir al archivo DLL de la interfaz de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**LÍNEA \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
</dt> </dl>

 

