---
description: El mensaje TSPI LINE SENDDIALOGINSTANCEDATA hace que TAPI llame a la función TUISPI providerGenericDialogData en el archivo DLL de interfaz de usuario asociado a \_ htDlgInst, pasando el bloque de parámetros al que apunta lpParams, de longitud \_ dwSize.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: LINE_SENDDIALOGINSTANCEDATA mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b955d890c385894467fa0f8f3f93ec50856c746c72f0957ecbe33af203917bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140138"
---
# <a name="line_senddialoginstancedata-message"></a>Mensaje \_ LINE SENDDIALOGINSTANCEDATA

El mensaje TSPI **LINE \_ SENDDIALOGINSTANCEDATA** hace que TAPI llame a la función [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) en el archivo DLL de interfaz de usuario asociado a *htDlgInst*, pasando el bloque de parámetros al que *apunta lpParams*, de longitud *dwSize*.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*htDlgInst* 
</dt> <dd>

HTAPIDIALOGINSTANCE que se devolvió al proveedor de servicios cuando se creó la instancia del cuadro de diálogo [**mediante LINE \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).

</dd> <dt>

*lpParams* 
</dt> <dd>

Puntero a un bloque de parámetros específico del proveedor que se transmite a la función [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) de LA DLL de la interfaz de usuario, cuyo tamaño especifica *dwSize*. Si este parámetro se establece en **NULL,** se trata de una solicitud para cerrar el cuadro de diálogo inmediatamente y limpiarlo (el archivo DLL de interfaz de usuario no debe invocar [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) durante esta limpieza).

</dd> <dt>

*dwSize* 
</dt> <dd>

Tamaño en bytes del bloque de parámetros que se va a transmitir al archivo DLL de la interfaz de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**Proveedor de \_ TUISPIGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**LINE \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
</dt> </dl>

 

