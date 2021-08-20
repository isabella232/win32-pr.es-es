---
title: Métodos de propiedad IADsPrintQueueOperations (Iads.h)
description: Los métodos de propiedad de la interfaz IADsPrintQueueOperations leen y escriben las propiedades enumeradas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea Métodos de propiedad de interfaz.
ms.assetid: a4e6bac5-5d52-4492-b48e-f051fec6158c
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad IADsPrintQueueOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintQueueOperations Property Methods
- IADsPrintQueueOperations.Status
- IADsPrintQueueOperations.get_Name
- IADsPrintQueueOperations.put_Name
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c0438491cb62d56584106d78f7639439d93d105fb635eeba0271759247f595
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839765"
---
# <a name="iadsprintqueueoperations-property-methods"></a>Métodos de propiedad IADsPrintQueueOperations

Los métodos de propiedad [**de la interfaz IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) leen y escriben las propiedades enumeradas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Estado**
</dt> <dd> <dl>

Estado actual de las operaciones de cola de impresión. Los valores de código de estado válidos se enumeran en la lista siguiente.

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

**ADS \_ IMPRESORA \_ EN PAUSA** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

**ADS \_ ELIMINACIÓN \_ PENDIENTE \_ DE IMPRESORA** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

**ADS \_ \_ERROR DE IMPRESORA** (0x00000003)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

**ADS \_ PAPEL \_ \_ DE IMPRESORA JAM** (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

**ADS \_ PAPEL \_ DE \_ IMPRESORA OUT** (0x00000005)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

**ADS \_ FUENTE \_ MANUAL \_ DE IMPRESORA** (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

**ADS \_ PROBLEMA \_ DE PAPEL DE \_ IMPRESORA** (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

**ADS \_ IMPRESORA \_ SIN CONEXIÓN** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

**ADS \_ IMPRESORA \_ \_ E/S ACTIVA** (0x00000100)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

**ADS \_ IMPRESORA \_ OCUPADA** (0x00000200)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

**ADS \_ IMPRESIÓN \_ DE IMPRESORA** (0x00000400)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

**ADS \_ BANDEJA \_ DE SALIDA DE IMPRESORA \_ \_ COMPLETA** (0x00000800)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

**ADS \_ IMPRESORA \_ NO \_ DISPONIBLE** (0x00001000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

**ADS \_ IMPRESORA \_ EN ESPERA** (0x00002000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

**ADS \_ PROCESAMIENTO \_ DE IMPRESORA** (0x00004000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

**ADS \_ INICIALIZACIÓN \_ DE IMPRESORA** (0x00008000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

**ADS \_ TEMPERATURA \_ DE \_ LA IMPRESORA** (0x00010000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

**ADS \_ TONER \_ DE IMPRESORA \_ BAJO** (0x00020000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

**ADS \_ IMPRESORA \_ SIN \_ TONER** (0x00040000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

**ADS \_ PUNT \_ DE \_ PÁGINA DE IMPRESORA** (0x00080000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

**ADS \_ INTERVENCIÓN \_ DEL \_ USUARIO DE** IMPRESORA (0x00100000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

**ADS \_ IMPRESORA \_ FUERA \_ DE \_ MEMORIA** (0x00200000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

**ADS \_ PRINTER \_ DOOR \_ OPEN** (0x00400000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

**ADS \_ SERVIDOR \_ DE IMPRESORA \_ DESCONOCIDO** (0x00800000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

**ADS \_ AHORRO \_ DE ENERGÍA DE \_ LA** IMPRESORA (0x01000000)


</dt> <dd></dd> </dl> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Name(
  [out] LONG* pbstrName
);
HRESULT put_Name(
  [in] LONG bstrName
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

En el Visual Basic ejemplo de código siguiente se comprueba que una impresora está atorada.


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



En el siguiente ejemplo de código de C++ se comprueba que una impresora está atorada.


```C++
IADsPrintQueueOperations *pqo;
HRESULT hr = ADsGetObject(L"WinNT://aMachine/aPrinter",
IID_IADsPrintQueueOperations,
(void**)&pqo)
long status;
hr = pqo->get_Status(&status);
if(status = ADS_PRINTER_PAPER_JAM) {
printf("Your printer is jammed.\n");
}
hr = pqo->Release();
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                              |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IADsPrintQueueOperations se define como 124BE5C0-156E-11CF-A986-00AA006BC149<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





