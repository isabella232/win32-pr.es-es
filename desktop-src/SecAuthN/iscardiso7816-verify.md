---
description: Construye un comando de unidad de datos de protocolo de aplicación (APDU) que inicia la comparación (en la tarjeta) de los datos de comprobación enviados desde el dispositivo de interfaz con los datos de referencia almacenados en la tarjeta (por ejemplo, contraseña).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: Método ISCardISO7816::Verify (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0d01fe47133ddeaf7bba32a91711d76783bdfbb0a28762d7ddb7f9054d0108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014445"
---
# <a name="iscardiso7816verify-method"></a>ISCardISO7816::Verify (método)

\[El **método Verify** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método Verify** crea un comando de unidad de datos de protocolo de aplicación (APDU) que inicia la comparación (en la tarjeta) de los datos de verificación enviados desde el dispositivo de interfaz con los datos de referencia almacenados en la tarjeta (por ejemplo, contraseña). [](../secgloss/a-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byRefCtrl* \[ En\]
</dt> <dd>

Cuantificador de los datos de referencia. A continuación se sigue la codificación del control de referencia P2.

Cuando el cuerpo está vacío, el comando se puede usar para recuperar el número "X" de reintentos permitidos adicionales (SW1-SW2=63CX) o para comprobar si la comprobación no es necesaria (SW1-SW2=9000).



| Value                                                                                                                                                                                    | Significado                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Sin información**</dt> </dl>                     | Posición del bit: 00000000<br/> P2=00 está reservado para indicar que no se usa ningún calificador determinado en esas tarjetas en las que el comando verify hace referencia a los datos secretos de forma inequívoca.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Referencia global**</dt> </dl>         | Posición de bits: 0-------<br/> Un ejemplo de referencia global sería una contraseña.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Referencia específica**</dt> </dl> | Posición de bits: 1-------<br/> Un ejemplo de ref específico es la contraseña específica de DF.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                           | Posición de bits: -xx-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Datos de referencia \#**</dt> </dl>        | Posición de bits: ---xxxxx<br/> El número de datos de referencia puede ser, por ejemplo, un número de contraseña o un identificador de EF corto.<br/>                                                           |



 

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Puntero a los datos de comprobación. Este parámetro puede ser **NULL**. El valor predeterminado es **NULL**.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **NULL.**

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se estableció en **NULL,** [*se*](../secgloss/s-gly.md) crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de tarjeta inteligente y se devuelve mediante el *puntero ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se ha completado correctamente.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se usó un parámetro que no es válido.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Se pasó un puntero no válido.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                          |



 

## <a name="remarks"></a>Comentarios

El estado de seguridad se puede modificar como resultado de una comparación. Se pueden registrar comparaciones incorrectas en la tarjeta (por ejemplo, para limitar el número de intentos lejos de usar los datos de referencia).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
