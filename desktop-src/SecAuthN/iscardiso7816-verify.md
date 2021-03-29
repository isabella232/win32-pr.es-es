---
description: Crea un comando APDU (unidad de datos de protocolo de aplicación) que inicia la comparación (en la tarjeta) de los datos de comprobación enviados desde el dispositivo de interfaz con los datos de referencia almacenados en la tarjeta (por ejemplo, contraseña).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'ISCardISO7816:: verify (método) (Scardssp. h)'
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
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652765"
---
# <a name="iscardiso7816verify-method"></a>ISCardISO7816:: verify (método)

\[El método **Verify** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **Verify** crea un comando de [*unidad de datos de protocolo de aplicación*](../secgloss/a-gly.md) (APDU) que inicia la comparación (en la tarjeta) de los datos de comprobación enviados desde el dispositivo de interfaz con los datos de referencia almacenados en la tarjeta (por ejemplo, password).

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

*byRefCtrl* \[ de\]
</dt> <dd>

Un cuantificador de los datos de referencia. A continuación se muestra la codificación del control de referencia P2.

Cuando el cuerpo está vacío, el comando se puede usar para recuperar el número ' X ' de reintentos más permitidos (SW1-SW2 = 63CX) o para comprobar si la comprobación no es necesaria (SW1-SW2 = 9000).



| Value                                                                                                                                                                                    | Significado                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Sin información**</dt> </dl>                     | Posición de bit: 00000000<br/> P2 = 00 está reservado para indicar que no se usa ningún calificador determinado en esas tarjetas donde el comando Verify hace referencia a los datos secretos de forma inequívoca.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Referencia global**</dt> </dl>         | Posición de bit: 0-------<br/> Un ejemplo de referencia global sería una contraseña.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Referencia específica**</dt> </dl> | Posición de bit: 1-------<br/> Un ejemplo de referencia específica es la contraseña específica de DF.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Posición de bit:-XX-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Datos de referencia \#**</dt> </dl>        | Posición de bit:---xxxxx<br/> El número de datos de referencia puede ser, por ejemplo, un número de contraseña o un identificador de EF corto.<br/>                                                           |



 

</dd> <dt>

*pdata* \[ de\]
</dt> <dd>

Puntero a los datos de comprobación. Este parámetro puede ser **NULL**. El valor predeterminado es **NULL**.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

En la entrada, puntero a un objeto de interfaz [**ISCardCmd**](iscardcmd.md) o **null**.

En la devolución, se rellena con el comando APDU construido por esta operación. Si *ppCmd* se ha establecido en **null**, se crea internamente un objeto [**ISCardCmd**](iscardcmd.md) de [*tarjeta inteligente*](../secgloss/s-gly.md) y se devuelve mediante el puntero *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | La operación se ha completado correctamente.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se usó un parámetro que no es válido.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Se pasó un puntero no válido.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                          |



 

## <a name="remarks"></a>Observaciones

El estado de seguridad puede modificarse como resultado de una comparación. Las comparaciones erróneas se pueden grabar en la tarjeta (por ejemplo, para limitar el número de intentos adicionales de uso de los datos de referencia).

Para obtener una lista de todos los métodos proporcionados por esta interfaz, vea [**ISCardISO7816**](iscardiso7816.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 se define como 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
