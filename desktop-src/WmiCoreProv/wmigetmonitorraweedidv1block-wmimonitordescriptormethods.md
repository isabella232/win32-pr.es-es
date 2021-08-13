---
description: Obtiene los datos sin procesar de una estructura de datos de identificación de pantalla extendida mejorada (E-EDID) de Video Electronics Standard Association (VESA) especificada que define la configuración óptima para configurar un monitor.
ms.assetid: a787e66e-1b96-4dd5-8646-7aa2d281ac95
title: Método WmiGetMonitorRawEEdidV1Block de la clase WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods.WmiGetMonitorRawEEdidV1Block
api_type:
- COM
api_location:
- WmiProv.dll
ms.openlocfilehash: dacd0c44a6c0fa8270a65155583f8041616f98674d0798db8b13a72d13751653
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118558090"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>Método WmiGetMonitorRawEEdidV1Block de la clase WmiMonitorDescriptorMethods

El **método WmiGetMonitorRawEEdidV1Block** obtiene los datos sin procesar de una estructura de datos de identificación de pantalla extendida (E-EDID) mejorada de Video Electronics Standard Association (VESA) especificada que define la configuración óptima para configurar un monitor.

## <a name="syntax"></a>Sintaxis


```mof
uint32 WmiGetMonitorRawEEdidV1Block(
  [in]  uint8 BlockId,
  [out] uint8 BlockType,
  [out] uint8 BlockContent[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BlockId* \[ En\]
</dt> <dd>

Identidad del bloque de datos.

</dd> <dt>

*BlockType* \[ out\]
</dt> <dd>

Tipo de bloque de datos. En la tabla siguiente se enumeran los posibles valores devueltos.



| Value                                                                                 | Significado                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>    | No inicializado<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Bloque base EDID<br/> |
| <dl> <dt>2 (0x2)</dt> </dl>    | Mapa de bloques EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Otros<br/>           |



 

</dd> <dt>

*BlockContent* \[ out\]
</dt> <dd>

Matriz de 128 bytes que contiene el contenido del bloque sin formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que se ha correcto. Cualquier otro número indica que hubo un error. Para obtener más información sobre los códigos de [**error,**](/windows/desktop/WmiSdk/wmi-error-constants) vea Constantes de error WMI o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se recuperan los bloques EDID de cualquier presentación como matrices sin formato de 128 bits.


```CSharp
static void Main(string[] args)
{
    ManagementClass mc = new ManagementClass(string.Format(@"\\{0}\root\wmi:WmiMonitorDescriptorMethods", Environment.MachineName));


    foreach (ManagementObject mo in mc.GetInstances()) //Do this for each connected monitor
    {              


        for (int i = 0; i < 256; i++)
        {
            ManagementBaseObject inParams = mo.GetMethodParameters("WmiGetMonitorRawEEdidV1Block");
            inParams["BlockId"] = i; 


            ManagementBaseObject outParams = null;
            try
            {
                outParams = mo.InvokeMethod("WmiGetMonitorRawEEdidV1Block", inParams, null);
                Console.Out.WriteLine("Returned a block of type {0}, having a content of type {1} ",
                                  outParams["BlockType"], outParams["BlockContent"].GetType());
            }
            catch { break; } //No more EDID blocks


                    
        }
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Espacio de nombres<br/>                | Wmi \\ raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

