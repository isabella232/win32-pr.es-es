---
title: Métodos de propiedad IADsPrintJobOperations (Iads.h)
description: Los métodos de propiedad de la interfaz IADsPrintJobOperations leen y escriben las propiedades enumeradas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea Métodos de propiedad de interfaz.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPrintJobOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70f337681cb7e75a478000bd06daaac1165edaaaf1cb4255b2890347fbcff7de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691074"
---
# <a name="iadsprintjoboperations-property-methods"></a>Métodos de propiedad IADsPrintJobOperations

Los métodos de propiedad [**de la interfaz IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) leen y escriben las propiedades enumeradas en la tabla siguiente. Para obtener más información sobre los métodos de propiedad, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**PagesPrinted**
</dt> <dd> <dl>

Contiene el número de páginas impresas.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

**Position**
</dt> <dd> <dl>

Contiene la posición de este trabajo de impresión en la cola de impresión.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

**Estado**
</dt> <dd> <dl>

Contiene el estado actual del trabajo de impresión tal como se indica en uno de los valores de Constantes de estado del trabajo de impresión [**ADSI.**](adsi-print-job-status-constants.md)

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

**TimeElapsed**
</dt> <dd> <dl>

Contiene el número de milisegundos transcurridos desde que se inició el trabajo de impresión.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra cómo se pueden usar las propiedades de [**IADsPrintJobOperations.**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                            |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsPrintJobOperations se define como 32FB6780-1ED0-11CF-A988-00AA006BC149<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**Constantes de estado del trabajo de impresión ADSI**](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





