---
description: Especifica un nuevo identificador de clase alternativa en la unidad de datos del protocolo de aplicación (APDU).
ms.assetid: 45a49699-41ce-439c-b896-e663a290b188
title: Método ISCardCmd::p ut_AlternateClassId (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_AlternateClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ee1ee5da5875ec2fa1f4f7f6e474f551befdaf8b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361862"
---
# <a name="iscardcmdput_alternateclassid-method"></a>Método ISCardCmd::p ut \_ AlternateClassId

\[El **método put \_ AlternateClassId** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método put \_ AlternateClassId** especifica un nuevo identificador de clase alternativa en la unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AlternateClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byClass* \[ En\]
</dt> <dd>

Identificador de clase alternativo. El valor predeterminado es cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operación completada correctamente.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro byClass* no es válido.<br/> |



 

## <a name="remarks"></a>Observaciones

Con las comunicaciones que usan el protocolo [*T=0,*](../secgloss/t-gly.md)la APDU puede generar automáticamente comandos de tarjeta adicionales y enviarlos a la unidad de datos del protocolo de transmisión (TPDU). Los comandos adicionales suelen usar el mismo identificador de clase que el comando original; La especificación de un nuevo identificador de clase mediante este método permite que los comandos generados automáticamente usen el nuevo identificador de clase.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer un nuevo identificador de clase alternativa en la unidad [*de datos del protocolo de aplicación*](../secgloss/a-gly.md) (APDU). En el ejemplo se supone que pISCardCmd es un puntero válido a una instancia de la [**interfaz ISCardCmd.**](iscardcmd.md)


```C++
HRESULT  hr;

// Set the class ID.
hr = pISCardCmd->put_AlternateClassId(0xC0);
if (FAILED(hr))
{
  printf("Failed put_AlternateClassId\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardCmd se define como \_ D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> <dt>

[**get \_ AlternateClassId**](iscardcmd-get-alternateclassid.md)
</dt> </dl>

 

 
