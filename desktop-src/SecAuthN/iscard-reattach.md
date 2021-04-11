---
description: El método volver a adjuntar restablece o reinicializa la tarjeta inteligente.
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'ISCard:: Reattach (método) (Scardmgr. h)'
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
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275917"
---
# <a name="iscardreattach-method"></a>ISCard:: Reattach (método)

\[El método para volver a **adjuntar** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método volver a **adjuntar** restablece o reinicializa la [*tarjeta inteligente*](../secgloss/s-gly.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ShareMode* \[ de\]
</dt> <dd>

Modo en el que se va a compartir o es el propietario exclusivo de la conexión a la tarjeta inteligente.



| Value                                                                                                                                            | Significado                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**ÚNICO**</dt> </dl> | Nadie más usa esta conexión con la tarjeta inteligente.<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**RECURSO**</dt> </dl>          | Otras aplicaciones pueden usar esta conexión.<br/>        |



 

</dd> <dt>

*InitState* \[ de\]
</dt> <dd>

Indica qué hacer con la tarjeta.



| Value                                                                                                                                      | Significado                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**OMITI**</dt> </dl>       | Deja la tarjeta inteligente en el [*Estado*](../secgloss/s-gly.md)actual.<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**DETERMINADO**</dt> </dl>       | Restablece la tarjeta inteligente a algún estado conocido.<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**No energía**</dt> </dl> | Quita la energía de la tarjeta inteligente.<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**EXPULSAR**</dt> </dl>       | Expulsa la tarjeta inteligente si el lector tiene capacidades de expulsión.<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Operación completada correctamente.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Hay un problema con uno o varios de los parámetros pasados a la función.<br/> |



 

## <a name="remarks"></a>Observaciones

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardmgr. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardmgr. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard se define como 1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**Conecta**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
