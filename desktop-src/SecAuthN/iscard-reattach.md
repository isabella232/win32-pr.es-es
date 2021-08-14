---
description: El método ReAttach restablece o reinicializa la tarjeta inteligente.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: Método ISCard::ReAttach (Scardmgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f28caee7a40574bf7f31fdc4fb55ddd81ea9e22cca12f1664950c96922d50902
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482115"
---
# <a name="iscardreattach-method"></a>ISCard::ReAttach (método)

\[El **método ReAttach** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método ReAttach** restablece o reinicializa la [*tarjeta inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShareMode* \[ En\]
</dt> <dd>

Modo en el que se va a compartir o poseer exclusivamente la conexión a la tarjeta inteligente.



| Value                                                                                                                                            | Significado                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**Exclusivo**</dt> </dl> | Nadie más usa esta conexión a la tarjeta inteligente.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**Compartido**</dt> </dl>          | Otras aplicaciones pueden usar esta conexión.<br/>        |



 

</dd> <dt>

*InitState* \[ En\]
</dt> <dd>

Indica qué hacer con la tarjeta.



| Value                                                                                                                                      | Significado                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**Salir**</dt> </dl>       | Deja la tarjeta inteligente en el estado [*actual.*](../secgloss/s-gly.md)<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**RESET**</dt> </dl>       | Restablece la tarjeta inteligente a un estado conocido.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**UNPOWER**</dt> </dl> | Quita la energía de la tarjeta inteligente.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**Expulsar**</dt> </dl>       | Expulsa la tarjeta inteligente si el lector tiene capacidades de expulsión.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operación completada correctamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Hay algún problema con uno o varios de los parámetros pasados a la función.<br/> |



 

## <a name="remarks"></a>Observaciones

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la reinicialización de la tarjeta inteligente.


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardmgr.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCard se define como \_ 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Desasociar**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
