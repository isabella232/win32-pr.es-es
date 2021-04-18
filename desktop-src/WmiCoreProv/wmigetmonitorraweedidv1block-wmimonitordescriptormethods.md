---
description: Obtiene los datos sin procesar de una estructura de datos de identificación mejorada de la presentación extendida (E-EDID) de vídeo electrónica estándar (VESA) que define los valores óptimos para configurar un monitor.
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
ms.openlocfilehash: 1af1ddb86a90ea9029d5cba408745fe3dafa69dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706941"
---
# <a name="wmigetmonitorraweedidv1block-method-of-the-wmimonitordescriptormethods-class"></a>Método WmiGetMonitorRawEEdidV1Block de la clase WmiMonitorDescriptorMethods

El método **WmiGetMonitorRawEEdidV1Block** obtiene los datos sin procesar de una estructura de datos de identificación mejorada de la presentación extendida (E-EDID) de vídeo electrónica de vídeo (VESA) que define la configuración óptima para la configuración de un monitor.

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

*BlockId* \[ de\]
</dt> <dd>

La identidad del bloque de datos.

</dd> <dt>

*BlockType* \[ enuncia\]
</dt> <dd>

Tipo de bloque de datos. En la tabla siguiente se enumeran los posibles valores devueltos.



| Value                                                                                 | Significado                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0 (0X0)</dt> </dl>    | No inicializado<br/>   |
| <dl> <dt>1 (0x1)</dt> </dl>    | Bloque base EDID<br/> |
| <dl> <dt>2 (0X2)</dt> </dl>    | Asignación de bloques EDID<br/>  |
| <dl> <dt>255 (0xFF)</dt> </dl> | Otros<br/>           |



 

</dd> <dt>

*BlockContent* \[ enuncia\]
</dt> <dd>

Una matriz de 128 bytes que contiene el contenido del bloque sin formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve cero (0) para indicar que la operación se ha realizado correctamente. Cualquier otro número indica que hubo un error. Para obtener más información sobre los códigos de error, vea [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se recuperan los bloques EDID de cualquier pantalla como matrices de 128 bits sin formato.


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
| Espacio de nombres<br/>                | \\WMI raíz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WmiMonitorDescriptorMethods**](wmimonitordescriptormethods.md)
</dt> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

