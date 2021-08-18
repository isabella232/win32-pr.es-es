---
description: El método SetDefaultClassId asigna un byte de identificador de clase estándar que se usará en todas las operaciones al construir una unidad de datos del protocolo de aplicación de comandos (APDU) ISO 7816-4. De forma predeterminada, el byte del identificador de clase estándar 0x00.
ms.assetid: 5a53d5f1-7986-4c4c-9512-f592cd398d1c
title: Método ISCardISO7816::SetDefaultClassId (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.SetDefaultClassId
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d242d83af00bb0d8e10d7da22d014a31deafaa66f49fb509cc91b65263239dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481130"
---
# <a name="iscardiso7816setdefaultclassid-method"></a>Método ISCardISO7816::SetDefaultClassId

\[El **método SetDefaultClassId** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método SetDefaultClassId** asigna un byte de identificador de clase estándar que se usará en todas las operaciones al construir una unidad de datos del protocolo de aplicación de comandos (APDU) ISO 7816-4. [](../secgloss/a-gly.md) De forma predeterminada, el byte del identificador de clase estándar 0x00.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDefaultClassId(
  [in] BYTE byClass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*byClass* \[ En\]
</dt> <dd>

Byte de identificador de clase.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Los valores devueltos posibles son los siguientes:



| Código devuelto                                                                          | Descripción                                  |
|--------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operación completada correctamente.<br/> |



 

Para obtener una lista de todos los métodos proporcionados por la [**interfaz ISCardISO7816,**](iscardiso7816.md) vea **ISCardISO7816**.

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de [*error*](../secgloss/s-gly.md) de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener información sobre los códigos de error de tarjeta inteligente, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
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

 

 
