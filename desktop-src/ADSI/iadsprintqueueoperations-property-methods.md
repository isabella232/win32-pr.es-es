---
title: Métodos de la propiedad IADsPrintQueueOperations (iAds. h)
description: Los métodos de propiedad de la interfaz IADsPrintQueueOperations leen y escriben las propiedades enumeradas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea métodos de propiedad de interfaz.
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
ms.openlocfilehash: a8af7aef94dd9453af690f0c5d83b1e978d3b058
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996828"
---
# <a name="iadsprintqueueoperations-property-methods"></a>Métodos de propiedad IADsPrintQueueOperations

Los métodos de propiedad de la interfaz [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations) leen y escriben las propiedades enumeradas en la lista siguiente. Para obtener más información sobre los métodos de propiedad, vea [métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**Estado**
</dt> <dd> <dl>

Estado actual de las operaciones de cola de impresión. Los valores de código de estado válidos se muestran en la lista siguiente.

<dt>

<span id="ADS_PRINTER_PAUSED"></span><span id="ads_printer_paused"></span>

**Anuncios \_ de IMPRESORA en \_ pausa** (0x00000001)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PENDING_DELETION"></span><span id="ads_printer_pending_deletion"></span>

**Anuncios \_ de \_ \_ Eliminación de impresora pendiente** (0x00000002)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_ERROR"></span><span id="ads_printer_error"></span>

**Anuncios \_ de \_Error de impresora** (0x00000003)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_JAM"></span><span id="ads_printer_paper_jam"></span>

**Anuncios \_ de \_ \_ Atasco de papel** de la impresora (0x00000004)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_OUT"></span><span id="ads_printer_paper_out"></span>

**Anuncios \_ de \_Papel \_** de la impresora (0x00000005)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_MANUAL_FEED"></span><span id="ads_printer_manual_feed"></span>

**Anuncios \_ de \_ \_ Alimentación manual** de la impresora (0x00000006)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAPER_PROBLEM"></span><span id="ads_printer_paper_problem"></span>

**Anuncios \_ de \_ \_ Problema de papel** de la impresora (0x00000007)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OFFLINE"></span><span id="ads_printer_offline"></span>

**Anuncios \_ de IMPRESORA \_ sin conexión** (0x00000008)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_IO_ACTIVE"></span><span id="ads_printer_io_active"></span>

**Anuncios \_ de \_E/ \_ s de impresora activa** (0x00000100)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_BUSY"></span><span id="ads_printer_busy"></span>

**Anuncios \_ de IMPRESORA \_ ocupada** (0x00000200)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PRINTING"></span><span id="ads_printer_printing"></span>

**Anuncios \_ de \_Impresión de impresora** (0x00000400)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUTPUT_BIN_FULL"></span><span id="ads_printer_output_bin_full"></span>

**Anuncios \_ de Bandeja de salida de impresora \_ \_ \_ completa** (0x00000800)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NOT_AVAILABLE"></span><span id="ads_printer_not_available"></span>

**Anuncios \_ de La impresora \_ no \_ está disponible** (0x00001000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WAITING"></span><span id="ads_printer_waiting"></span>

**Anuncios \_ de IMPRESORA en \_ espera** (0x00002000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PROCESSING"></span><span id="ads_printer_processing"></span>

**Anuncios \_ de \_Procesamiento** de la impresora (0x00004000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_INITIALIZING"></span><span id="ads_printer_initializing"></span>

**Anuncios \_ de \_Inicialización** de la impresora (0x00008000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_WARMING_UP"></span><span id="ads_printer_warming_up"></span>

**Anuncios \_ de \_Preparación \_ de la impresora** (0x00010000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_TONER_LOW"></span><span id="ads_printer_toner_low"></span>

**Anuncios \_ de Tóner de impresora \_ \_ bajo** (0x00020000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_NO_TONER"></span><span id="ads_printer_no_toner"></span>

**Anuncios \_ de IMPRESORA \_ sin \_ tóner** (0x00040000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_PAGE_PUNT"></span><span id="ads_printer_page_punt"></span>

**Anuncios \_ de Página de la impresora \_ \_ aparcan** (0x00080000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_USER_INTERVENTION"></span><span id="ads_printer_user_intervention"></span>

**Anuncios \_ de \_ \_ Intervención del usuario** de la impresora (0x00100000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_OUT_OF_MEMORY"></span><span id="ads_printer_out_of_memory"></span>

**Anuncios \_ de \_ \_ \_ Memoria insuficiente de la impresora** (0x00200000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_DOOR_OPEN"></span><span id="ads_printer_door_open"></span>

**Anuncios \_ de IMPRESORA de \_ puerta \_ abierta** (0x00400000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_SERVER_UNKNOWN"></span><span id="ads_printer_server_unknown"></span>

**Anuncios \_ de Servidor de impresora \_ \_ desconocido** (0x00800000)


</dt> <dd></dd> <dt>

<span id="ADS_PRINTER_POWER_SAVE"></span><span id="ads_printer_power_save"></span>

**Anuncios \_ de Ahorro \_ de \_ energía** de la impresora (0x01000000)


</dt> <dd></dd> </dl> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Tipo de datos de scripting: **largo**
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

En el siguiente ejemplo de código Visual Basic se comprueba que se ha atascado una impresora.


```VB
Dim pqo As IADsPrintQueueOperations
Set pqo = GetObject("WinNT://aMachine/aPrinter")
If pqo.Status = ADS_PRINTER_PAPER_JAM Then
MsgBox "Your printer is jammed."
End If
```



En el siguiente ejemplo de código de C++ se comprueba que una impresora está atascada.


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



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>IAds. h</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>     |
| IID<br/>                      | IID \_ IADsPrintQueueOperations se define como 124BE5C0-156E-11cf-A986-00AA006BC149<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)
</dt> </dl>

 

 





